---
UID: NF:dpa_dsa.DPA_SaveStream
title: DPA_SaveStream function
author: windows-driver-content
description: Saves the dynamic pointer array (DPA) to a stream by writing out a header, and then calling the specified callback function to write each element.
old-location: controls\DPA_SaveStream.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_savestream.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DPA_SaveStream, DPA_SaveStream function [Windows Controls], _win32_DPA_SaveStream, _win32_DPA_SaveStream_cpp, controls.DPA_SaveStream, controls._win32_DPA_SaveStream, dpa_dsa/DPA_SaveStream
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComCtl32.dll
api_name:
-	DPA_SaveStream
product: Windows
targetos: Windows
req.lib: 
req.dll: ComCtl32.dll
req.irql: 
---

# DPA_SaveStream function


## -description


<p class="CCE_Message">[<b>DPA_SaveStream</b> is available in Windows Vista. It might be altered or unavailable in subsequent versions. ]

Saves the dynamic pointer array (DPA) to a stream by writing out a header, and then calling the specified callback function to write each element.


## -parameters




### -param hdpa

TBD


### -param pfn [in]

Type: <b><a href="https://msdn.microsoft.com/b5910ac3-9066-49d8-8cb3-796de22428d3">PFNDPASTREAM</a></b>

The callback function. See <a href="https://msdn.microsoft.com/b5910ac3-9066-49d8-8cb3-796de22428d3">PFNDPASTREAM</a> for the callback function prototype. 


### -param pstream

TBD


### -param pvInstData [in]

Type: <b>void*</b>

A pointer to callback data. <i>pvInstData</i> is passed as a parameter to <i>pfn</i>. 


#### - pdpa [in]

Type: <b>HDPA</b>

Receives a handle to a DPA.


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
Indicates that the callback function was unsuccessful in saving the element; however, the process should continue. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that even though the callback was unsuccessful, the process was uninterrupted. 

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
</table>
 




## -remarks



This function must be called directly from ComCtl32.dll. It is ordinal 10.

The callback is responsible for writing the <i>pvInstData</i> data to the stream.



