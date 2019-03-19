---
UID: NC:ntsecpkg.LSA_CALL_PACKAGEEX
title: LSA_CALL_PACKAGEEX (ntsecpkg.h)
author: windows-sdk-content
description: The CallPackageEx function is used to call another security package to access its services.
old-location: security\callpackageex.htm
tech.root: SecAuthN
ms.assetid: b26eb42d-9692-4df7-bbde-f7bce0924221
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CallPackageEx, CallPackageEx callback function [Security], LSA_CALL_PACKAGEEX, LSA_CALL_PACKAGEEX callback, _ssp_callpackageex, ntsecpkg/CallPackageEx, security.callpackageex
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - CallPackageEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LSA_CALL_PACKAGEEX callback function


## -description


The <b>CallPackageEx</b> function is used to call another <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to access its services.


## -parameters




### -param AuthenticationPackage [in]

Pointer to a 
<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> containing the name of the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> to call.


### -param ClientBufferBase [in]

The base address of the input buffer, in the client's address space.


### -param ProtocolSubmitBuffer [in]

Pointer to the input buffer.


### -param SubmitBufferLength [in]

Size of <i>ProtocolSubmitBuffer</i>, in bytes.


### -param *ProtocolReturnBuffer [out]

Pointer that receives the address of the output buffer.


### -param ReturnBufferLength [out]

Pointer to a variable that receives the size of <i>ProtocolReturnBuffer</i>, in bytes.


### -param ProtocolStatus [out]

Pointer to a variable that receives the status code returned by the authentication package.


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
The <i>AuthenticationPackage</i> parameter does not contain the name of a valid security package.

</td>
</tr>
</table>
 




## -remarks



A pointer to the <b>CallPackageEx</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/770c41ab-df79-4371-9f1d-7bbce8193b5d">CallPackage</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

