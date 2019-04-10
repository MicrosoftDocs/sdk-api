---
UID: NF:certenc.ICertEncodeLongArray.Decode
title: ICertEncodeLongArray::Decode (certenc.h)
author: windows-sdk-content
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded Long array and stores the resulting array of Long values in the CertEncodeLongArray object.
old-location: security\icertencodelongarray_decode.htm
tech.root: SecCrypto
ms.assetid: b0ff8e1a-c4b2-48ac-be95-228638d00e6d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CCertEncodeLongArray object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeLongArray object, Decode method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],Decode method, ICertEncodeLongArray.Decode, ICertEncodeLongArray::Decode, _certsrv_icertencodelongarray_decode, certenc/ICertEncodeLongArray::Decode, security.icertencodelongarray_decode
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
 - ICertEncodeLongArray.Decode
 - CCertEncodeLongArray.Decode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeLongArray::Decode


## -description


The <b>Decode</b> method decodes an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1)-encoded <b>Long</b> array and stores the resulting array of <b>Long</b> values in the <b>CertEncodeLongArray</b> object.


## -parameters




### -param strBinary [in]

An ASN.1-encoded <b>Long</b> array.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method places the decoded contents of <i>strBinary</i> into the object's array of <b>Long</b> values. If the object's array already contains <b>Long</b> values, the existing content will be freed, and the array will be loaded with the decoded values.


#### Examples

For an example that uses the <b>Decode</b> method, see the <a href="https://msdn.microsoft.com/e2cf6e69-2431-4a97-86f1-9e1546aa6c08">ICertEncodeLongArray::Encode</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e8555282-6c09-4f23-830e-358bc73287ee">ICertEncodeLongArray</a>



<a href="https://msdn.microsoft.com/e2cf6e69-2431-4a97-86f1-9e1546aa6c08">ICertEncodeLongArray::Encode</a>
 

 

