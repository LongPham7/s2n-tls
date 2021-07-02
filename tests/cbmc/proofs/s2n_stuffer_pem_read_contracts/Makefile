# Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License"). You may not use
# this file except in compliance with the License. A copy of the License is
# located at
#
#     http://aws.amazon.com/apache2.0/
#
# or in the "license" file accompanying this file. This file is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
# implied. See the License for the specific language governing permissions and
# limitations under the License.

# The function s2n_stuffer_pem_read_contents in s2n_stuffer_pem.c contains a 
# loop that is annotated with a loop invariant and a decreases clause. 
APPLY_LOOP_CONTRACTS=1

PROOF_UID = s2n_stuffer_pem_read_contracts
HARNESS_ENTRY = $(PROOF_UID)_harness
HARNESS_FILE = $(HARNESS_ENTRY).c

PROOF_SOURCES += $(PROOFDIR)/$(HARNESS_FILE)
PROOF_SOURCES += $(PROOF_SOURCE)/make_common_datastructures.c

PROJECT_SOURCES += $(SRCDIR)/stuffer/s2n_stuffer_pem.c
PROJECT_SOURCES += $(SRCDIR)/stuffer/s2n_stuffer_base64.c
PROJECT_SOURCES += $(SRCDIR)/stuffer/s2n_stuffer.c

PROJECT_SOURCES += $(SRCDIR)/utils/s2n_blob.c
PROJECT_SOURCES += $(SRCDIR)/error/s2n_errno.c
PROJECT_SOURCES += $(SRCDIR)/utils/s2n_result.c
PROJECT_SOURCES += $(SRCDIR)/utils/s2n_ensure.c

include ../Makefile.common
