---
UID: NC:ntsecpkg.LSA_CREATE_LOGON_SESSION
title: LSA_CREATE_LOGON_SESSION
author: windows-driver-content
description: Creates logon sessions.
old-location: security\createlogonsession.htm
old-project: SecAuthN
ms.assetid: 383c935c-a1f2-4d1b-bb02-e7e37f154771
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CreateLogonSession, CreateLogonSession function [Security], LSA_CREATE_LOGON_SESSION, _lsa_createlogonsession, ntsecpkg/CreateLogonSession, security.createlogonsession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	CreateLogonSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_CREATE_LOGON_SESSION callback function


## -description


Creates logon sessions.

The logon session is identified by a unique logon ID (
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>) assigned to the logon session.


## -parameters




### -param LogonId [in]

Pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure to be assigned to the new logon session. An authentication package calls 
<a href="https://msdn.microsoft.com/5d730034-802b-4d37-bd28-68992779b93e">AllocateLocallyUniqueId</a> in order to generate this ID.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_LOGON_SESSION_COLLISION</b></dt>
</dl>
</td>
<td width="60%">
The specified logon ID is already in use by another logon session.

</td>
</tr>
</table>
 

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



If an authentication package creates extraneous logon sessions while determining whether to authenticate the user, it should delete them by calling 
<a href="https://msdn.microsoft.com/72b9451c-8a94-4e64-bd78-0afef210671c">DeleteLogonSession</a>. If the authentication fails, the authentication package should delete all related logon sessions.

Because logon sessions use memory in the kernel, it is important to delete any unused or discarded logon sessions.




## -see-also




<a href="https://msdn.microsoft.com/72b9451c-8a94-4e64-bd78-0afef210671c">DeleteLogonSession</a>



<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

