---
UID: NS:ntsecpkg._LSA_TOKEN_INFORMATION_V1
title: LSA_TOKEN_INFORMATION_V1 (ntsecpkg.h)
description: Contains information an authentication package can place in a Version 2 Windows token object and has superceded LSA_TOKEN_INFORMATION_V1.
helpviewer_keywords: ["*PLSA_TOKEN_INFORMATION_V1","*PLSA_TOKEN_INFORMATION_V2","LSA_TOKEN_INFORMATION_V1","LSA_TOKEN_INFORMATION_V2","LSA_TOKEN_INFORMATION_V2 structure [Security]","PLSA_TOKEN_INFORMATION_V2","PLSA_TOKEN_INFORMATION_V2 structure pointer [Security]","_LSA_TOKEN_INFORMATION_V1","ntsecpkg/LSA_TOKEN_INFORMATION_V2","ntsecpkg/PLSA_TOKEN_INFORMATION_V2","security.lsa_token_information_v2"]
old-location: security\lsa_token_information_v2.htm
tech.root: security
ms.assetid: 6BEDAC01-99DA-4EE5-9667-A11E00BE7A30
ms.date: 12/05/2018
ms.keywords: '*PLSA_TOKEN_INFORMATION_V1, *PLSA_TOKEN_INFORMATION_V2, LSA_TOKEN_INFORMATION_V1, LSA_TOKEN_INFORMATION_V2, LSA_TOKEN_INFORMATION_V2 structure [Security], PLSA_TOKEN_INFORMATION_V2, PLSA_TOKEN_INFORMATION_V2 structure pointer [Security], _LSA_TOKEN_INFORMATION_V1, ntsecpkg/LSA_TOKEN_INFORMATION_V2, ntsecpkg/PLSA_TOKEN_INFORMATION_V2, security.lsa_token_information_v2'
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LSA_TOKEN_INFORMATION_V1, *PLSA_TOKEN_INFORMATION_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_TOKEN_INFORMATION_V1
 - ntsecpkg/_LSA_TOKEN_INFORMATION_V1
 - PLSA_TOKEN_INFORMATION_V1
 - ntsecpkg/PLSA_TOKEN_INFORMATION_V1
 - LSA_TOKEN_INFORMATION_V1
 - ntsecpkg/LSA_TOKEN_INFORMATION_V1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - LSA_TOKEN_INFORMATION_V2
---

# LSA_TOKEN_INFORMATION_V1 structure


## -description

The <b>LSA_TOKEN_INFORMATION_V2</b> structure contains information an <a href="/windows/desktop/SecGloss/a-gly">authentication package</a> can place in a Version 2 Windows token object and has superceded <a href="/previous-versions/windows/desktop/legacy/aa378721(v=vs.85)">LSA_TOKEN_INFORMATION_V1</a>.

The version 2 token information is used in most logons. The structure is identical to the <a href="/previous-versions/windows/desktop/legacy/aa378721(v=vs.85)">LSA_TOKEN_INFORMATION_V1</a> structure, with the exception that the memory allocation is handled differently. The <b>LSA_TOKEN_INFORMATION_V2</b> structure is intended to be allocated monolithically with the privileges, DACL, SIDs, and group array either part of the same allocation, or allocated and freed externally.

A Version 2 Windows token object stores all the information needed to build a token from the authentication package to the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA). The LSA passes this information into the kernel to create a token object and to return a handle to that token object to the caller of <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>.

## -struct-fields

### -field ExpirationTime

Time at which the <a href="/windows/desktop/SecGloss/s-gly">security context</a> becomes not valid. Use a value in the distant future if the context never expires. The current version of the operating system kernel does not enforce this expiration time.

### -field User

<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a> structure that contains the SID of the user logging on. The <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> SID value is in a separately allocated block of memory.

### -field Groups

<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure that contains the SIDs of groups the user is a member of. This should not include WORLD or other system-defined and system-assigned SIDs. These will be added automatically by the LSA. 




Each SID is expected to be in a separately allocated block of memory. The <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure is also expected to be in a separately allocated block of memory. All of these memory blocks should be allocated by calling the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_allocate_private_heap">AllocatePrivateHeap</a> function.

### -field PrimaryGroup

<a href="/windows/desktop/api/winnt/ns-winnt-token_primary_group">TOKEN_PRIMARY_GROUP</a> structure that is used to establish the primary group of the user. This value does not have to correspond to one of the SIDs assigned to the user. 




The SID pointed to by this structure is expected to be in a separately allocated block of memory.

This member is mandatory and must be filled in.

### -field Privileges

<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure that contains the <a href="/windows/desktop/SecGloss/p-gly">privileges</a> assigned to the user. This list of privileges will be augmented or overridden by any local security policy assigned privileges. 




Each privilege is expected to be in a separately allocated block of memory. The <a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a> structure is also expected to be in a separately allocated block of memory.

If there are no privileges to assign to the user, this member may be set to <b>NULL</b>.

### -field Owner

<a href="/windows/desktop/api/winnt/ns-winnt-token_owner">TOKEN_OWNER</a> structure. This member may be used to establish an explicit default owner. Normally, the user ID is used as the default owner. If another value is desired, it must be specified here. 




The <b>Owner.Sid</b> member may be set to <b>NULL</b> to indicate there is no alternate default owner value.

### -field DefaultDacl

<a href="/windows/desktop/api/winnt/ns-winnt-token_default_dacl">TOKEN_DEFAULT_DACL</a> structure. This member may be used to establish a default protection for the user. If no value is provided, a default protection that grants everyone all access will be established. 




The <b>DefaultDacl.DefaultDacl</b> member may be set to <b>NULL</b> to indicate there is no default protection.