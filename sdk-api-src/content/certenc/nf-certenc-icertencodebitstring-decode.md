---
UID: NF:certenc.ICertEncodeBitString.Decode
title: ICertEncodeBitString::Decode
author: windows-sdk-content
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded bit string and stores the resulting bit string in this object.
old-location: security\icertencodebitstring_decode.htm
old-project: SecCrypto
ms.assetid: 65856db4-97db-4c9b-ac12-1a9262c7b4e9
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CCertEncodeBitString object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeBitString object, Decode method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],Decode method, ICertEncodeBitString.Decode, ICertEncodeBitString::Decode, _certsrv_icertencodebitstring_decode, certenc/ICertEncodeBitString::Decode, security.icertencodebitstring_decode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenc.h
req.include-header: Certsrv.h
req.redist: 
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
tech.root: 
req.typenames: X509EnrollmentAuthFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeBitString.Decode
 - CCertEncodeBitString.Decode
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# ICertEncodeBitString::Decode


## -description


The <b>Decode</b> method decodes an <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1)-encoded bit string and stores the resulting bit string in this object. You can then call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa383893(v=VS.85).aspx">ICertEncodeBitString::GetBitCount</a> and 
<a href="https://msdn.microsoft.com/en-us/library/Aa383899(v=VS.85).aspx">ICertEncodeBitString::GetBitString</a> methods to retrieve the bit string and its size.


## -parameters




### -param strBinary [in]

An ASN.1-encoded bit string.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



Use this method to decode an encoded bit string.


#### Examples

For an example that calls the <b>Decode</b> method, see the <a href="https://msdn.microsoft.com/en-us/library/Aa383878(v=VS.85).aspx">ICertEncodeBitString::Encode</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383767(v=VS.85).aspx">ICertEncodeBitString</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383878(v=VS.85).aspx">ICertEncodeBitString::Encode</a>
 

 

