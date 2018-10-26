---
UID: NF:certenc.ICertEncodeStringArray.SetValue
title: ICertEncodeStringArray::SetValue
author: windows-sdk-content
description: Sets a string value at the specified index of the string array.
old-location: security\icertencodestringarray_setvalue.htm
tech.root: seccrypto
ms.assetid: 41e5c2b8-a0da-426a-b411-0bdc3fd7ecfe
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CCertEncodeStringArray object [Security],SetValue method, ICertEncodeStringArray interface [Security],SetValue method, ICertEncodeStringArray.SetValue, ICertEncodeStringArray::SetValue, SetValue, SetValue method [Security], SetValue method [Security],CCertEncodeStringArray object, SetValue method [Security],ICertEncodeStringArray interface, _certsrv_icertencodestringarray_setvalue, certenc/ICertEncodeStringArray::SetValue, security.icertencodestringarray_setvalue
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
 - ICertEncodeStringArray.SetValue
 - CCertEncodeStringArray.SetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeStringArray::SetValue


## -description


The <b>SetValue</b> method sets a string value at the specified index of the string array.

 You must call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa385019(v=VS.85).aspx">ICertEncodeStringArray::Reset</a> method before calling <b>SetValue</b> for the first time.


## -parameters




### -param Index [in]

The zero-based index that specifies the element of the string array to set.


### -param str [in]

Specifies the string value to set.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385013(v=VS.85).aspx">ICertEncodeStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385019(v=VS.85).aspx">ICertEncodeStringArray::Reset</a>
 

 

