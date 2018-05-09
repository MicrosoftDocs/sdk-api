---
UID: NS:ntsecpkg._LSA_TOKEN_INFORMATION_V1
title: "_LSA_TOKEN_INFORMATION_V1"
author: windows-driver-content
description: Contains information an authentication package can place in a Version 1 Windows token object.
old-location: security\lsa_token_information_v1.htm
old-project: SecAuthN
ms.assetid: e4c43828-aa5c-443c-93ad-96bb986533c5
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PLSA_TOKEN_INFORMATION_V1, *PLSA_TOKEN_INFORMATION_V2, LSA_TOKEN_INFORMATION_V1, LSA_TOKEN_INFORMATION_V1 structure [Security], LSA_TOKEN_INFORMATION_V2, PLSA_TOKEN_INFORMATION_V1, PLSA_TOKEN_INFORMATION_V1 structure pointer [Security], _LSA_TOKEN_INFORMATION_V1, _lsa_lsa_token_information_v1, ntsecpkg/LSA_TOKEN_INFORMATION_V1, ntsecpkg/PLSA_TOKEN_INFORMATION_V1, security.lsa_token_information_v1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: LSA_TOKEN_INFORMATION_V1, *PLSA_TOKEN_INFORMATION_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecpkg.h
api_name:
-	LSA_TOKEN_INFORMATION_V1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _LSA_TOKEN_INFORMATION_V1 structure


## -description


The <b>LSA_TOKEN_INFORMATION_V1</b> structure contains information an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> can place in a Version 1 Windows token object.

The version 1 token information has been superceded by <a href="https://msdn.microsoft.com/6BEDAC01-99DA-4EE5-9667-A11E00BE7A30">LSA_TOKEN_INFORMATION_V2</a> and <a href="https://msdn.microsoft.com/927828CD-9763-4CE4-B3E7-376181EA7C70">LSA_TOKEN_INFORMATION_V3</a> structures.

A Version 1 Windows token object stores all the information needed to build a token from the authentication package to the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA). The LSA passes this information into the kernel to create a token object and to return a handle to that token object to the caller of <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


## -struct-fields




### -field ExpirationTime

Time at which the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> becomes not valid. Use a value in the distant future if the context never expires. The current version of the operating system kernel does not enforce this expiration time.


### -field User


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a> structure that contains the SID of the user logging on. The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> SID value is in a separately allocated block of memory.


### -field Groups


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure that contains the SIDs of groups the user is a member of. This should not include WORLD or other system-defined and system-assigned SIDs. These will be added automatically by the LSA. 




Each SID is expected to be in a separately allocated block of memory. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure is also expected to be in a separately allocated block of memory. All of these memory blocks should be allocated by calling the <a href="https://msdn.microsoft.com/956e7aaf-e8b3-4db5-945a-b579f946b769">AllocatePrivateHeap</a> function.


### -field PrimaryGroup


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556845">TOKEN_PRIMARY_GROUP</a> structure that is used to establish the primary group of the user. This value does not have to correspond to one of the SIDs assigned to the user. 




The SID pointed to by this structure is expected to be in a separately allocated block of memory.

This member is mandatory and must be filled in.


### -field Privileges


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a> structure that contains the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> assigned to the user. This list of privileges will be augmented or overridden by any local security policy assigned privileges. 




Each privilege is expected to be in a separately allocated block of memory. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a> structure is also expected to be in a separately allocated block of memory.

If there are no privileges to assign to the user, this member may be set to <b>NULL</b>.


### -field Owner


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556842">TOKEN_OWNER</a> structure. This member may be used to establish an explicit default owner. Normally, the user ID is used as the default owner. If another value is desired, it must be specified here. 




The <b>Owner.Sid</b> member may be set to <b>NULL</b> to indicate there is no alternate default owner value.


### -field DefaultDacl


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556831">TOKEN_DEFAULT_DACL</a> structure. This member may be used to establish a default protection for the user. If no value is provided, a default protection that grants everyone all access will be established. 




The <b>DefaultDacl.DefaultDacl</b> member may be set to <b>NULL</b> to indicate there is no default protection.

