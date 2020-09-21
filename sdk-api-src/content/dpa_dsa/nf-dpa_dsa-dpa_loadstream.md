---
UID: NF:dpa_dsa.DPA_LoadStream
title: DPA_LoadStream function (dpa_dsa.h)
description: Loads the dynamic pointer array (DPA) from a stream by calling the specified callback function to read each element.
helpviewer_keywords: ["DPA_LoadStream","DPA_LoadStream function [Windows Controls]","_win32_DPA_LoadStream","_win32_DPA_LoadStream_cpp","controls.DPA_LoadStream","controls._win32_DPA_LoadStream","dpa_dsa/DPA_LoadStream"]
old-location: controls\DPA_LoadStream.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_loadstream.htm
ms.date: 12/05/2018
ms.keywords: DPA_LoadStream, DPA_LoadStream function [Windows Controls], _win32_DPA_LoadStream, _win32_DPA_LoadStream_cpp, controls.DPA_LoadStream, controls._win32_DPA_LoadStream, dpa_dsa/DPA_LoadStream
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: ComCtl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DPA_LoadStream
 - dpa_dsa/DPA_LoadStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_LoadStream
---

# DPA_LoadStream function


## -description

<p class="CCE_Message">[<b>DPA_LoadStream</b> is available in Windows Vista. It might be altered or unavailable in subsequent versions. ]

Loads the dynamic pointer array (DPA) from a stream by calling the specified callback function to read each element.

## -parameters

### -param phdpa [out]

Type: <b>HDPA*</b>

A handle to a DPA.

### -param pfn [in]

Type: <b><a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpastream">PFNDPASTREAM</a></b>

The callback function. See <a href="/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpastream">PFNDPASTREAM</a> for the callback function prototype.

### -param pstream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object.

### -param pvInstData [in]

Type: <b>void*</b>

A pointer to callback data. <i>pvInstData</i> is passed as a parameter to <i>pfn</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the callback function was successful and the element was loaded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the callback function was unsuccessful in loading the element; however, the process should continue. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that one or more of the parameters is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the stream object could not be read. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The buffer length is invalid or there was insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

This function must be called directly from ComCtl32.dll. It is ordinal 9.

The callback is responsible for writing the <i>pvInstData</i> data to the stream.