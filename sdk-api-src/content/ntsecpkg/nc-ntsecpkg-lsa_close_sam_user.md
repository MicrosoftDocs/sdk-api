---
UID: NC:ntsecpkg.LSA_CLOSE_SAM_USER
title: LSA_CLOSE_SAM_USER
author: windows-sdk-content
description: Closes a handle to a Security Accounts Manager (SAM) user account.
old-location: security\closesamuser.htm
old-project: SecAuthN
ms.assetid: 1e56e38e-ba8f-4781-80f1-e60bd33250e4
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CloseSamUser, CloseSamUser function [Security], LSA_CLOSE_SAM_USER, _ssp_closesamuser, ntsecpkg/CloseSamUser, security.closesamuser
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	CloseSamUser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_CLOSE_SAM_USER callback function


## -description


The <b>CloseSamUser</b> function closes a handle to a Security Accounts Manager (SAM) user account.


## -parameters




### -param UserHandle [in]

A handle to the SAM user account previously opened using the 
<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a> function.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason. The following table lists a common reason for failure and the error code that the function returns.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified for <i>UserHandle</i> is not valid or <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



A pointer to the <b>CloseSamUser</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

