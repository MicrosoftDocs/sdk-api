---
UID: NF:certenc.ICertEncodeStringArray.Encode
title: ICertEncodeStringArray::Encode
author: windows-sdk-content
description: Returns an ASN.1-encoded string of the string array stored in this object.
old-location: security\icertencodestringarray_encode.htm
tech.root: seccrypto
ms.assetid: d8fc51ea-4d83-402a-a4ac-ce55d385905c
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CCertEncodeStringArray object [Security],Encode method, Encode, Encode method [Security], Encode method [Security],CCertEncodeStringArray object, Encode method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],Encode method, ICertEncodeStringArray.Encode, ICertEncodeStringArray::Encode, _certsrv_icertencodestringarray_encode, certenc/ICertEncodeStringArray::Encode, security.icertencodestringarray_encode
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
 - ICertEncodeStringArray.Encode
 - CCertEncodeStringArray.Encode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeStringArray::Encode


## -description


The <b>Encode</b> method returns an ASN.1-encoded string of the string array stored in this object.

Use the <a href="https://msdn.microsoft.com/en-us/library/Aa385014(v=VS.85).aspx">Decode</a> method to decode the encoded string into an <b>CertEncodeStringArray</b> object.

 Before using this method, you must call the <a href="https://msdn.microsoft.com/en-us/library/Aa385019(v=VS.85).aspx">Reset</a> to size the array and the 
<a href="https://msdn.microsoft.com/en-us/library/Aa385020(v=VS.85).aspx">SetValue</a> method to set each string in the array.


## -parameters




### -param pstrBinary

TBD




#### - pbstrBinary [out]

A pointer to a <b>BSTR</b> that will contain the encoded string array. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the ASN.1-encoded string array.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385013(v=VS.85).aspx">ICertEncodeStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385014(v=VS.85).aspx">ICertEncodeStringArray::Decode</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385019(v=VS.85).aspx">ICertEncodeStringArray::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385020(v=VS.85).aspx">ICertEncodeStringArray::SetValue</a>
 

 

