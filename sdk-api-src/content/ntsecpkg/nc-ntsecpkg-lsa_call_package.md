---
UID: NC:ntsecpkg.LSA_CALL_PACKAGE
title: LSA_CALL_PACKAGE
author: windows-driver-content
description: The CallPackage function is used to call another security package to access its services.
old-location: security\callpackage.htm
old-project: SecAuthN
ms.assetid: 770c41ab-df79-4371-9f1d-7bbce8193b5d
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CallPackage, CallPackage function [Security], LSA_CALL_PACKAGE, _ssp_callpackage, ntsecpkg/CallPackage, security.callpackage
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
-	CallPackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_CALL_PACKAGE callback function


## -description


The <b>CallPackage</b> function is used to call another <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to access its services.


## -parameters




### -param AuthenticationPackage [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the name of the package to call.


### -param ProtocolSubmitBuffer [in]

Pointer to the input buffer. The content of this buffer is package-specific.


### -param SubmitBufferLength [in]

Size of the <i>ProtocolSubmitBuffer</i> parameter in bytes.


### -param *ProtocolReturnBuffer [out]

Pointer that receives the address of the output buffer. The content of this buffer is package-specific.


### -param ReturnBufferLength [out]

Pointer to a variable that receives the size of the <i>ProtocolReturnBuffer</i> parameter in bytes.


### -param ProtocolStatus [out]

Pointer to a variable that receives the status code returned by the called package.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed. The following table lists a common reason for failure and the error code that the function returns.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>AuthenticationPackage</i> parameter does not contain the name of a valid <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

</td>
</tr>
</table>
 




## -remarks



A pointer to the <b>CallPackage</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b26eb42d-9692-4df7-bbde-f7bce0924221">CallPackageEx</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

