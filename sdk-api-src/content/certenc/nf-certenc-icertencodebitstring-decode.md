---
UID: NF:certenc.ICertEncodeBitString.Decode
title: ICertEncodeBitString::Decode (certenc.h)
author: windows-sdk-content
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded bit string and stores the resulting bit string in this object.
old-location: security\icertencodebitstring_decode.htm
tech.root: SecCrypto
ms.assetid: 65856db4-97db-4c9b-ac12-1a9262c7b4e9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CCertEncodeBitString object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeBitString object, Decode method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],Decode method, ICertEncodeBitString.Decode, ICertEncodeBitString::Decode, _certsrv_icertencodebitstring_decode, certenc/ICertEncodeBitString::Decode, security.icertencodebitstring_decode
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
 - ICertEncodeBitString.Decode
 - CCertEncodeBitString.Decode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeBitString::Decode


## -description


The <b>Decode</b> method decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded bit string and stores the resulting bit string in this object. You can then call the 
<a href="https://msdn.microsoft.com/9fbaaf03-02b8-4c6f-8cc2-3fd897fdc81d">ICertEncodeBitString::GetBitCount</a> and 
<a href="https://msdn.microsoft.com/d0c6c501-3aaa-42ab-a077-69f6d24f1eff">ICertEncodeBitString::GetBitString</a> methods to retrieve the bit string and its size.


## -parameters




### -param strBinary [in]

An ASN.1-encoded bit string.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Use this method to decode an encoded bit string.


#### Examples

For an example that calls the <b>Decode</b> method, see the <a href="https://msdn.microsoft.com/2dc74ab4-8f40-4e0d-a18e-ba9c99d5bf94">ICertEncodeBitString::Encode</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/51178b67-46da-49f8-9bd7-a500e846e0a8">ICertEncodeBitString</a>



<a href="https://msdn.microsoft.com/2dc74ab4-8f40-4e0d-a18e-ba9c99d5bf94">ICertEncodeBitString::Encode</a>
 

 

