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

# IWMResizerProps::GetFullCropRegion


## -description



Retrieves the source and destination rectangles.



## -parameters




### -param lClipOriXSrc [out]

Receives the left edge of the source rectangle, in pixels.


### -param lClipOriYSrc [out]

Receives the top edge of the source rectangle, in pixels.


### -param lClipWidthSrc [out]

Receives the width of the source rectangle, in pixels.


### -param lClipHeightSrc [out]

Receives the height of the source rectangle, in pixels.


### -param lClipOriXDst [out]

Receives the left edge of the destination rectangle, in pixels.


### -param lClipOriYDst [out]

Receives the top edge of the destination rectangle, in pixels.


### -param lClipWidthDst [out]

Receives the width of the destination rectangle, in pixels.


### -param lClipHeightDst [out]

Receives the height of the destination rectangle, in pixels.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/12c26507-c729-4143-a0bd-e043d42744f6">IWMResizerProps Interface</a>
 

 

