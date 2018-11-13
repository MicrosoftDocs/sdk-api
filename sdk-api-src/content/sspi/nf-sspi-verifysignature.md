---
UID: NF:sspi.VerifySignature
title: VerifySignature function
author: windows-sdk-content
description: Verifies that a message signed by using the MakeSignature function was received in the correct sequence and has not been modified.
old-location: security\verifysignature.htm
tech.root: secauthn
ms.assetid: bebeef92-1d6e-4879-846f-12d706db0653
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: VerifySignature, VerifySignature function [Security], _ssp_verifysignature, security.verifysignature, sspi/VerifySignature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - VerifySignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VerifySignature function


## -description


Verifies that a message signed by using the 
<a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> function was received in the correct sequence and has not been modified.


## -parameters




### -param phContext [in]

A handle to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> to use for the message.


### -param pMessage [in]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that references a set of 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures that contain the message and signature to verify. The signature is in a <b>SecBuffer</b> structure of type SECBUFFER_TOKEN.


### -param MessageSeqNo [in]

Specifies the sequence number expected by the transport application, if any. If the transport application does not maintain sequence numbers, this parameter is zero.


### -param pfQOP [out]

Pointer to a <b>ULONG</b> variable that receives package-specific flags that indicate the quality of protection.

Some security packages ignore this parameter.


## -returns



If the function verifies that the message was received in the correct sequence and has not been modified, the return value is SEC_E_OK.

If the function determines that the message is not correct according to the information in the signature, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The message was not received in the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_MESSAGE_ALTERED</b></dt>
</dl>
</td>
<td width="60%">
The message has been altered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The context handle specified by <i>phContext</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
<i>pMessage</i> did not contain a valid SECBUFFER_TOKEN buffer, or contained too few buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_QOP_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The quality of protection negotiated between the client and server did not include <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">integrity</a> checking.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Warning</b>  <p class="note">The <b>VerifySignature</b> function will fail if the message was signed using the <a href="https://msdn.microsoft.com/98d71de2-6209-4182-ae58-4d0765731540">RsaSignPssSha512</a> algorithm on a different version of Windows. For example, a message that was signed by calling the <a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> function on Windows 8 will cause the <b>VerifySignature</b> function on Windows 8.1 to fail.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>
 

 

