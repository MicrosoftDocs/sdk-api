---
UID: NF:dpa_dsa.DPA_LoadStream
title: DPA_LoadStream function
author: windows-sdk-content
description: Loads the dynamic pointer array (DPA) from a stream by calling the specified callback function to read each element.
old-location: controls\DPA_LoadStream.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_loadstream.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DPA_LoadStream, DPA_LoadStream function [Windows Controls], _win32_DPA_LoadStream, _win32_DPA_LoadStream_cpp, controls.DPA_LoadStream, controls._win32_DPA_LoadStream, dpa_dsa/DPA_LoadStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_LoadStream
product: Windows
targetos: Windows
req.lib: 
req.dll: ComCtl32.dll
req.irql: 
---

# DPA_LoadStream function


## -description


<p class="CCE_Message">[<b>DPA_LoadStream</b> is available in Windows Vista. It might be altered or unavailable in subsequent versions. ]

Loads the dynamic pointer array (DPA) from a stream by calling the specified callback function to read each element.


## -parameters




### -param phdpa

TBD


### -param pfn [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb775725(v=VS.85).aspx">PFNDPASTREAM</a></b>

The callback function. See <a href="https://msdn.microsoft.com/library/Bb775725(v=VS.85).aspx">PFNDPASTREAM</a> for the callback function prototype. 


### -param pstream

TBD


### -param pvInstData [in]

Type: <b>void*</b>

A pointer to callback data. <i>pvInstData</i> is passed as a parameter to <i>pfn</i>. 


#### - ppdpa [out]

Type: <b>HDPA*</b>

A handle to a DPA.


#### - pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

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



