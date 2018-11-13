---
UID: NF:certenc.ICertEncodeLongArray.SetValue
title: ICertEncodeLongArray::SetValue
author: windows-sdk-content
description: Sets a Long value at the specified index of the Long array.
old-location: security\icertencodelongarray_setvalue.htm
tech.root: seccrypto
ms.assetid: 021b2539-3226-4893-af76-9b7b1637e12e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertEncodeLongArray object [Security],SetValue method, ICertEncodeLongArray interface [Security],SetValue method, ICertEncodeLongArray.SetValue, ICertEncodeLongArray::SetValue, SetValue, SetValue method [Security], SetValue method [Security],CCertEncodeLongArray object, SetValue method [Security],ICertEncodeLongArray interface, _certsrv_icertencodelongarray_setvalue, certenc/ICertEncodeLongArray::SetValue, security.icertencodelongarray_setvalue
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
 - ICertEncodeLongArray.SetValue
 - CCertEncodeLongArray.SetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertEncodeLongArray::SetValue


## -description


The <b>SetValue</b> method sets a <b>Long</b> value at the specified index of the <b>Long</b> array.

 You must call 
<a href="https://msdn.microsoft.com/en-us/library/Aa385010(v=VS.85).aspx">ICertEncodeLongArray::Reset</a> before calling <b>SetValue</b> for the first time.


## -parameters




### -param Index [in]

The zero-based index that specifies the index of the array element to set.


### -param Value [in]

Specifies the <b>Long</b> value to set.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa384997(v=VS.85).aspx">ICertEncodeLongArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385007(v=VS.85).aspx">ICertEncodeLongArray::GetValue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385010(v=VS.85).aspx">ICertEncodeLongArray::Reset</a>
 

 

