---
UID: NF:infocard.Encrypt
title: Encrypt function
author: windows-driver-content
description: Derives a session key from the secret and encrypts the Content property value using that key. It returns the encrypted content as an encoded string.
old-location: security\encrypteddata_encrypt.htm
old-project: SecCrypto
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CAPICOM_ENCODE_ANY, CAPICOM_ENCODE_BASE64, CAPICOM_ENCODE_BINARY, Encrypt, Encrypt method [Security], Encrypt method [Security], EncryptedData object, EncryptedData object [Security], Encrypt method, _crypto2_encrypteddata.encrypt, security.encrypteddata_encrypt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: infocard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TEXT_SOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Capicom.dll
api_name:
-	EncryptedData.Encrypt
product: Windows
targetos: Windows
req.lib: 
req.dll: Capicom.dll
req.irql: 
req.product: GDI+ 1.1
---

# Encrypt function


## -description


<p class="CCE_Message">[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP. Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions <a href="https://msdn.microsoft.com/927f2e9a-96cf-4744-bd57-420b5034d28d">CryptEncryptMessage</a> and <a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a> to encrypt and decrypt messages. For information about PInvoke, see <a href="http://go.microsoft.com/fwlink/p/?linkid=119531">Platform Invoke Tutorial</a>. The <a href="netcryptoapi">.NET and CryptoAPI via P/Invoke: Part 1</a> and <a href="netcryptoapi">.NET and CryptoAPI via P/Invoke: Part 2</a> subsections of <a href="netcryptoapi">Extending .NET Cryptography with CAPICOM and P/Invoke</a> may also be helpful.]

The <b>Encrypt</b> method derives a session key from the secret and encrypts the <a href="https://msdn.microsoft.com/fdab0f19-c69e-443b-b4b3-079d23028921">Content</a> property value using that key. It returns the encrypted content as an encoded string.


## -parameters




### -param hCrypto

TBD


### -param fOAEP

TBD


### -param cbInData

TBD


### -param pInData

TBD


### -param pcbOutData

TBD


### -param ppOutData

TBD




#### - EncodingType [in, optional]

A value of the
						<a href="https://msdn.microsoft.com/13e78a5e-3a31-44de-b249-28e360e1e087">CAPICOM_ENCODING_TYPE</a>  enumeration that indicates  the encoding type used to encode the encrypted data. The default value is CAPICOM_ENCODE_BASE64. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CAPICOM_ENCODE_ANY"></a><a id="capicom_encode_any"></a><dl>
<dt><b>CAPICOM_ENCODE_ANY</b></dt>
</dl>
</td>
<td width="60%">
This encoding type is used only when the input data has an unknown encoding type. If this value is used to specify the output's encoding type, CAPICOM_ENCODE_BASE64 will be used instead. Introduced in CAPICOM 2.0.

</td>
</tr>
<tr>
<td width="40%"><a id="CAPICOM_ENCODE_BASE64"></a><a id="capicom_encode_base64"></a><dl>
<dt><b>CAPICOM_ENCODE_BASE64</b></dt>
</dl>
</td>
<td width="60%">
Data is saved as a base64-encoded string.

</td>
</tr>
<tr>
<td width="40%"><a id="CAPICOM_ENCODE_BINARY"></a><a id="capicom_encode_binary"></a><dl>
<dt><b>CAPICOM_ENCODE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Data is saved as a pure binary sequence.

</td>
</tr>
</table>
 


## -returns



A string  that contains the encrypted, encoded data.
						
					




## -remarks



Before calling the <b>Encrypt</b> method, set the <a href="https://msdn.microsoft.com/fdab0f19-c69e-443b-b4b3-079d23028921">Content</a> property and call the <a href="https://msdn.microsoft.com/d940ae0b-a697-4529-b494-0051b9a6db5e">SetSecret</a> method.




## -see-also




<a href="https://msdn.microsoft.com/4ab16355-1341-4c7a-b570-bd33f11dde00">Cryptography Objects</a>



<a href="https://msdn.microsoft.com/3b9bd0a2-6e15-4d58-a682-588a93895799">EncryptedData</a>
 

 

