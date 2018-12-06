---
UID: NF:certenc.ICertEncodeStringArray.Decode
title: ICertEncodeStringArray::Decode
author: windows-sdk-content
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded string array and stores the resulting array of strings in the CertEncodeStringArray object.
old-location: security\icertencodestringarray_decode.htm
tech.root: seccrypto
ms.assetid: 35799b54-2c04-4bb4-a227-d2902b2379ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertEncodeStringArray object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeStringArray object, Decode method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],Decode method, ICertEncodeStringArray.Decode, ICertEncodeStringArray::Decode, _certsrv_icertencodestringarray_decode, certenc/ICertEncodeStringArray::Decode, security.icertencodestringarray_decode
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICertEncodeStringArray.Decode
 - CCertEncodeStringArray.Decode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeStringArray::Decode


## -description


The <b>Decode</b> method decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded string array and stores the resulting array of strings in the <b>CertEncodeStringArray</b> object.


## -parameters




### -param strBinary [in]

An ASN.1-encoded string array. 


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method will place the decoded contents of <i>strBinary</i> into the object's array of strings. If the object's array already contains strings, this existing content will be freed, and the array will be loaded with the decoded values.


#### Examples

For an example that uses the <b>Decode</b> method, see the <a href="https://msdn.microsoft.com/d8fc51ea-4d83-402a-a4ac-ce55d385905c">ICertEncodeStringArray::Encode</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5515c25e-f788-4222-8f66-f5d86bd2a3a3">ICertEncodeStringArray</a>



<a href="https://msdn.microsoft.com/d8fc51ea-4d83-402a-a4ac-ce55d385905c">ICertEncodeStringArray::Encode</a>
 

 

