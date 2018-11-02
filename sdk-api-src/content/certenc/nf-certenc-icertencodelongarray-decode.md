---
UID: NF:certenc.ICertEncodeLongArray.Decode
title: ICertEncodeLongArray::Decode
author: windows-sdk-content
description: Decodes an Abstract Syntax Notation One (ASN.1)-encoded Long array and stores the resulting array of Long values in the CertEncodeLongArray object.
old-location: security\icertencodelongarray_decode.htm
tech.root: seccrypto
ms.assetid: b0ff8e1a-c4b2-48ac-be95-228638d00e6d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CCertEncodeLongArray object [Security],Decode method, Decode, Decode method [Security], Decode method [Security],CCertEncodeLongArray object, Decode method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],Decode method, ICertEncodeLongArray.Decode, ICertEncodeLongArray::Decode, _certsrv_icertencodelongarray_decode, certenc/ICertEncodeLongArray::Decode, security.icertencodelongarray_decode
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
 - ICertEncodeLongArray.Decode
 - CCertEncodeLongArray.Decode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeLongArray::Decode


## -description


The <b>Decode</b> method decodes an <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1)-encoded <b>Long</b> array and stores the resulting array of <b>Long</b> values in the <b>CertEncodeLongArray</b> object.


## -parameters




### -param strBinary [in]

An ASN.1-encoded <b>Long</b> array.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



This method places the decoded contents of <i>strBinary</i> into the object's array of <b>Long</b> values. If the object's array already contains <b>Long</b> values, the existing content will be freed, and the array will be loaded with the decoded values.


#### Examples

For an example that uses the <b>Decode</b> method, see the <a href="https://msdn.microsoft.com/en-us/library/Aa385003(v=VS.85).aspx">ICertEncodeLongArray::Encode</a> method.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa384997(v=VS.85).aspx">ICertEncodeLongArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385003(v=VS.85).aspx">ICertEncodeLongArray::Encode</a>
 

 

