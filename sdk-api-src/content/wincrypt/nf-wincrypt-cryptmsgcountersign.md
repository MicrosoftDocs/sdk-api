---
UID: NF:wincrypt.CryptMsgCountersign
title: CryptMsgCountersign function
author: windows-sdk-content
description: Countersigns an existing signature in a message.
old-location: security\cryptmsgcountersign.htm
tech.root: seccrypto
ms.assetid: ebf76664-bca6-462d-b519-2b60f435d8ef
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CryptMsgCountersign, CryptMsgCountersign function [Security], _crypto2_cryptmsgcountersign, security.cryptmsgcountersign, wincrypt/CryptMsgCountersign
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptMsgCountersign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptMsgCountersign function


## -description


The <b>CryptMsgCountersign</b> function countersigns an existing signature in a message. <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Countersignatures</a> are used to sign an existing signature's encrypted <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the message. Countersignatures can be used for various purposes including time stamping a message.


## -parameters




### -param hCryptMsg [in, out]

Cryptographic message handle to be used.


### -param dwIndex [in]

Zero-based index of the signer in the signed or signed-and-enveloped message to be countersigned.


### -param cCountersigners [in]

Number of countersigners in the <i>rgCountersigners</i> array.


### -param rgCountersigners [in]

Array of countersigners' 
<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structures.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

An error can be propagated from
								<a href="https://msdn.microsoft.com/d9fd734b-e14d-4392-ac88-5565aefbedb4">CryptMsgCountersignEncoded</a>.

The following error codes are returned most often.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The specified area is not large enough to hold the returned data.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/d9fd734b-e14d-4392-ac88-5565aefbedb4">CryptMsgCountersignEncoded</a>



<a href="https://msdn.microsoft.com/b0332360-a737-4b48-b592-0c55d493a02d">CryptMsgVerifyCountersignatureEncoded</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Low-level Message Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

