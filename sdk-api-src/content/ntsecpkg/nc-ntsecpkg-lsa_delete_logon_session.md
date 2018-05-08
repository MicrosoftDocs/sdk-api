---
UID: NC:ntsecpkg.LSA_DELETE_LOGON_SESSION
title: LSA_DELETE_LOGON_SESSION
author: windows-driver-content
description: Cleans up any logon sessions created while determining whether a user's authentication information is legitimate.
old-location: security\deletelogonsession.htm
old-project: SecAuthN
ms.assetid: 72b9451c-8a94-4e64-bd78-0afef210671c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: DeleteLogonSession, DeleteLogonSession function [Security], LSA_DELETE_LOGON_SESSION, _lsa_deletelogonsession, ntsecpkg/DeleteLogonSession, security.deletelogonsession
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
-	DeleteLogonSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_DELETE_LOGON_SESSION callback function


## -description


Cleans up any logon sessions created while determining whether a user's authentication information is legitimate.

If the authentication fails, the authentication package should delete all related logon sessions.


## -parameters




### -param LogonId [in]

Pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure containing the session ID of logon session to delete.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BAD_LOGON_SESSION_STATE</b></dt>
</dl>
</td>
<td width="60%">
The specified logon session has a reference count value that prevents it from being deleted. This is a serious problem, caused by both the operating system and authentication package believing they have authority over the logon session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_LOGON_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The specified logon session could not be found.

</td>
</tr>
</table>
 

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



Because logon sessions use up memory in the kernel, any unused or discarded logon sessions should be deleted. However, logon sessions should not be deleted after a logon ID for the session has been returned to the LSA. After the LSA has been given a logon ID (for example, as a result of a 
<a href="https://msdn.microsoft.com/4c8def77-d536-486e-a830-9df3848fbccb">LsaApLogonUser</a> call), the LSA assumes it is responsible for the logon session and will delete it when the operating system no longer needs it. At this time, the LSA calls 
<a href="https://msdn.microsoft.com/17e8426a-5a25-48ca-8cef-91bbeda8490c">LsaApLogonTerminated</a> to notify the authentication package that the session has been deleted.

In contrast, authentication packages are not notified when a logon session is deleted with <b>DeleteLogonSession</b>.




## -see-also




<a href="https://msdn.microsoft.com/383c935c-a1f2-4d1b-bb02-e7e37f154771">CreateLogonSession</a>



<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

