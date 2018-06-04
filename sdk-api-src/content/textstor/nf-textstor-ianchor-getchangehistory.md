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

# IAnchor::GetChangeHistory


## -description


The <b>IAnchor::GetChangeHistory</b> method gets the history of deletions that have occurred immediately preceding or following the anchor.


## -parameters




### -param pdwHistory [out]

Bit field flags that specify that deletions have occurred immediately preceding or following the anchor. One or both of the following values can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_CH_PRECEDING_DEL"></a><a id="ts_ch_preceding_del"></a><dl>
<dt><b>TS_CH_PRECEDING_DEL</b></dt>
</dl>
</td>
<td width="60%">
Text preceding the anchor has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_CH_FOLLOWING_DEL"></a><a id="ts_ch_following_del"></a><dl>
<dt><b>TS_CH_FOLLOWING_DEL</b></dt>
</dl>
</td>
<td width="60%">
Text following the anchor has been deleted.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pdwHistory</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



The <i>pdwHistory</i> change flags must be set when deletions adjacent to the anchor have occurred.

The change flags remain set until they are cleared with a call to <a href="https://msdn.microsoft.com/3780ab3d-6b77-45bc-9630-747fa5caaecc">IAnchor::ClearChangeHistory</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/3780ab3d-6b77-45bc-9630-747fa5caaecc">IAnchor::ClearChangeHistory
      </a>
 

 

