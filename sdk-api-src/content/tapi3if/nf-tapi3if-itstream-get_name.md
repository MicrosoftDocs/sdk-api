---
UID: NF:tapi3if.ITStream.get_Name
title: ITStream::get_Name (tapi3if.h)
description: The get_Name method gets a BSTR representing the name of the stream. This name is used for informational or display purposes.
helpviewer_keywords: ["ITStream interface [TAPI 2.2]","get_Name method","ITStream.get_Name","ITStream::get_Name","_tapi3_itstream_get_name","get_Name","get_Name method [TAPI 2.2]","get_Name method [TAPI 2.2]","ITStream interface","tapi3.itstream_get_name","tapi3if/ITStream::get_Name"]
old-location: tapi3\itstream_get_name.htm
tech.root: tapi3
ms.assetid: b3b81bd7-f99a-4cb1-8d60-6be8c1e68722
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],get_Name method, ITStream.get_Name, ITStream::get_Name, _tapi3_itstream_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITStream interface, tapi3.itstream_get_name, tapi3if/ITStream::get_Name
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITStream::get_Name
 - tapi3if/ITStream::get_Name
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITStream.get_Name
---

# ITStream::get_Name


## -description

The 
<b>get_Name</b> method gets a <b>BSTR</b> representing the name of the stream. This name is used for informational or display purposes.

## -parameters

### -param ppName [out]

Pointer to <b>BSTR</b> representation of stream's name.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppName</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>