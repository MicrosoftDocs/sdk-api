---
UID: NF:certenc.ICertEncodeAltName.Encode
title: ICertEncodeAltName::Encode (certenc.h)
author: windows-sdk-content
description: Returns an ASN.1-encoded string of the alternate name array stored in this object. The names in the object are not encoded.
old-location: security\icertencodealtname_encode.htm
tech.root: SecCrypto
ms.assetid: 34136053-1c25-4f6b-8bd6-699fffb6670b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertEncodeAltName object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeAltName object, Encode method [Security],ICertEncodeAltName interface, ICertEncodeAltName interface [Security],Encode method, ICertEncodeAltName.Encode, ICertEncodeAltName::Encode, _certsrv_icertencodealtname_encode, certenc/ICertEncodeAltName::Encode, security.icertencodealtname_encode
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
 - ICertEncodeAltName.Encode
 - CCertEncodeAltName.Encode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeAltName::Encode


## -description


The <b>Encode</b> method returns an ASN.1-encoded string of the alternate name array stored in this object. The names in the object are not encoded.

Use the <a href="https://msdn.microsoft.com/0507d3a5-b8c3-4f2e-996f-e1e32957f475">Decode</a> method to decode the encoded string into an <b>CertEncodeAltName</b> object.

Before using this method, you must call both the 
<a href="https://msdn.microsoft.com/99aa43fe-534b-4696-8bfc-7049b16be1cf">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/5da07c09-9213-4604-b058-5e69df646b09">SetNameEntry</a> method to set each array element.


## -parameters




### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that receives the ASN.1-encoded alternate name extension. When done, call <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free <i>pbstrBinary</i>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded alternate name array.




## -see-also




<a href="https://msdn.microsoft.com/e0ecfcb0-f2ca-4e1c-a054-c83c03d55465">ICertEncodeAltName</a>



<a href="https://msdn.microsoft.com/0507d3a5-b8c3-4f2e-996f-e1e32957f475">ICertEncodeAltName::Decode</a>



<a href="https://msdn.microsoft.com/99aa43fe-534b-4696-8bfc-7049b16be1cf">ICertEncodeAltName::Reset</a>



<a href="https://msdn.microsoft.com/5da07c09-9213-4604-b058-5e69df646b09">ICertEncodeAltName::SetNameEntry</a>
 

 

