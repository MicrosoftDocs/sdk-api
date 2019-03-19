---
UID: NF:certenc.ICertEncodeBitString.Encode
title: ICertEncodeBitString::Encode (certenc.h)
author: windows-sdk-content
description: Performs Abstract Syntax Notation One (ASN.1) encoding on a given bit string.
old-location: security\icertencodebitstring_encode.htm
tech.root: SecCrypto
ms.assetid: 2dc74ab4-8f40-4e0d-a18e-ba9c99d5bf94
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertEncodeBitString object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeBitString object, Encode method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],Encode method, ICertEncodeBitString.Encode, ICertEncodeBitString::Encode, _certsrv_icertencodebitstring_encode, certenc/ICertEncodeBitString::Encode, security.icertencodebitstring_encode
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeBitString.Encode
 - CCertEncodeBitString.Encode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeBitString::Encode


## -description


The <b>Encode</b> method performs <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding on a given bit string.


## -parameters




### -param BitCount [in]

The number of bits in <i>strBitString</i>.


### -param strBitString [in]

The bit string to encode.


### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded bit string. When you have finished using this <b>BSTR</b>, call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to free <i>pbstrBinary</i>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded bit string.




## -see-also




<a href="https://msdn.microsoft.com/51178b67-46da-49f8-9bd7-a500e846e0a8">ICertEncodeBitString</a>



<a href="https://msdn.microsoft.com/65856db4-97db-4c9b-ac12-1a9262c7b4e9">ICertEncodeBitString::Decode</a>
 

 

