---
UID: NF:certenc.ICertEncodeStringArray.GetValue
title: ICertEncodeStringArray::GetValue
author: windows-sdk-content
description: Returns the specified string from the string array.
old-location: security\icertencodestringarray_getvalue.htm
tech.root: seccrypto
ms.assetid: 93f827c6-4dc6-462f-8865-eb631d7fe7bc
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CCertEncodeStringArray object [Security],GetValue method, GetValue, GetValue method [Security], GetValue method [Security],CCertEncodeStringArray object, GetValue method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],GetValue method, ICertEncodeStringArray.GetValue, ICertEncodeStringArray::GetValue, _certsrv_icertencodestringarray_getvalue, certenc/ICertEncodeStringArray::GetValue, security.icertencodestringarray_getvalue
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
 - ICertEncodeStringArray.GetValue
 - CCertEncodeStringArray.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeStringArray::GetValue


## -description


The <b>GetValue</b> method returns the specified string from the string array.


## -parameters




### -param Index [in]

The zero-based index that specifies the string to retrieve.


### -param pstr [out]

A pointer to a <b>BSTR</b> that represents the string value. When you have finished using the <b>BSTR</b>, free it by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the string value at the specified index.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385013(v=VS.85).aspx">ICertEncodeStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385017(v=VS.85).aspx">ICertEncodeStringArray::GetStringType</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385020(v=VS.85).aspx">ICertEncodeStringArray::SetValue</a>
 

 

