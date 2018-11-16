---
UID: NF:certenc.ICertEncodeLongArray.Encode
title: ICertEncodeLongArray::Encode
author: windows-sdk-content
description: Returns an ASN.1-encoded string of the LONG array stored in this object.
old-location: security\icertencodelongarray_encode.htm
tech.root: SecCrypto
ms.assetid: e2cf6e69-2431-4a97-86f1-9e1546aa6c08
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CCertEncodeLongArray object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeLongArray object, Encode method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],Encode method, ICertEncodeLongArray.Encode, ICertEncodeLongArray::Encode, _certsrv_icertencodelongarray_encode, certenc/ICertEncodeLongArray::Encode, security.icertencodelongarray_encode
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
 - ICertEncodeLongArray.Encode
 - CCertEncodeLongArray.Encode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenc.h
: 
- ICertEncodeLongArray.Encode
: 
---

# ICertEncodeLongArray::Encode


## -description


The <b>Encode</b> method returns an ASN.1-encoded string of the <b>LONG</b> array stored in this object.

Use the <a href="https://msdn.microsoft.com/b0ff8e1a-c4b2-48ac-be95-228638d00e6d">Decode</a> method to decode the encoded string into an <b>CertEncodeLongArray</b> object.

Before calling the <b>Encode</b> method, you must call the 
<a href="https://msdn.microsoft.com/4b5821e0-c81a-47b7-98b0-2a293967d8f6">Reset</a> method to size the array and the 
<a href="https://msdn.microsoft.com/021b2539-3226-4893-af76-9b7b1637e12e">SetValue</a> method to set each <b>LONG</b> value in the array.


## -parameters




### -param pstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded <b>LONG</b> array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is the ASN.1-encoded <b>LONG</b> array.




## -see-also




<a href="https://msdn.microsoft.com/e8555282-6c09-4f23-830e-358bc73287ee">ICertEncodeLongArray</a>



<a href="https://msdn.microsoft.com/b0ff8e1a-c4b2-48ac-be95-228638d00e6d">ICertEncodeLongArray::Decode</a>



<a href="https://msdn.microsoft.com/4b5821e0-c81a-47b7-98b0-2a293967d8f6">ICertEncodeLongArray::Reset</a>



<a href="https://msdn.microsoft.com/021b2539-3226-4893-af76-9b7b1637e12e">ICertEncodeLongArray::SetValue</a>
 

 

