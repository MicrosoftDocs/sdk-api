---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAnchor::ShiftRegion


## -description




## -parameters




### -param dwFlags [in]

Bitfields that are used to control anchor repositioning around hidden text, or to avoid actual repositioning of the anchor.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_SHIFT_COUNT_HIDDEN"></a><a id="ts_shift_count_hidden"></a><dl>
<dt><b>TS_SHIFT_COUNT_HIDDEN</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region. If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_SHIFT_COUNT_ONLY"></a><a id="ts_shift_count_only"></a><dl>
<dt><b>TS_SHIFT_COUNT_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The anchor is not shifted.

</td>
</tr>
</table>
 


### -param dir [in]

Contains one of the <a href="https://msdn.microsoft.com/e247b79d-354c-4211-9160-e705436d669c">TsShiftDir</a> values that specifies which adjacent region the anchor is moved to.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_SD_BACKWARD"></a><a id="ts_sd_backward"></a><dl>
<dt><b>TS_SD_BACKWARD</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the anchor will be moved to the region immediately preceding a range of text.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_SD_FORWARD"></a><a id="ts_sd_forward"></a><dl>
<dt><b>TS_SD_FORWARD</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the anchor will be moved to the region immediately following a range of text.

</td>
</tr>
</table>
 


### -param pfNoRegion [out]

Boolean value that specifies whether a shift of the anchor occurred.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The shift failed, and the anchor was not repositioned.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The shift succeeded.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The shift failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An input parameter value is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/e57a78e6-42e6-4a2b-b4e1-20bb64add872">
        IAnchor::Shift
      </a>



<a href="https://msdn.microsoft.com/93329238-f6e8-432e-9167-550a02b33b46">
        TS_SHIFT_* Constants
      </a>



<a href="https://msdn.microsoft.com/e247b79d-354c-4211-9160-e705436d669c">TsShiftDir
      </a>
 

 

