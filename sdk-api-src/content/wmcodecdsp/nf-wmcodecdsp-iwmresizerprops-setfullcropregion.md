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

# IWMResizerProps::SetFullCropRegion


## -description



Sets the source and destination rectangles.



## -parameters




### -param lClipOriXSrc [in]

Specifies the left edge of the source rectangle, in pixels.


### -param lClipOriYSrc [in]

Specifies the top edge of the source rectangle, in pixels.


### -param lClipWidthSrc [in]

Specifies the width of the source rectangle, in pixels.


### -param lClipHeightSrc [in]

Specifies the height of the source rectangle, in pixels.


### -param lClipOriXDst [in]

Specifies the left edge of the destination rectangle, in pixels.


### -param lClipOriYDst [in]

Specifies the top edge of the destination rectangle, in pixels.


### -param lClipWidthDst [in]

Specifies the width of the destination rectangle, in pixels.


### -param lClipHeightDst [in]

Specifies the height of the destination rectangle, in pixels.


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
 




## -remarks



By default, the video resizer copies the entire video frame. When you call this method, the video resizer crops the video to the source rectangle and copies that portion to the destination rectangle.

This method is equivalent to setting the following properties:

<ul>
<li>
<a href="https://msdn.microsoft.com/e7432b80-f3fa-4c2f-89db-87cd130d7447">MFPKEY_RESIZE_SRC_LEFT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/12791b9f-4b00-4697-ae3c-8fc069568c82">MFPKEY_RESIZE_SRC_TOP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1c527040-6673-4753-905b-8c74c1ae0d59">MFPKEY_RESIZE_SRC_WIDTH</a>
</li>
<li>
<a href="https://msdn.microsoft.com/418bcd69-9dde-4bc3-9897-f465d12536a1">MFPKEY_RESIZE_SRC_HEIGHT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/faefe634-c517-43a0-9741-cb79824f840d">MFPKEY_RESIZE_DST_LEFT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/66147460-b8c2-4d80-9a87-a2eeeea66cfa">MFPKEY_RESIZE_DST_TOP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8f0066ca-c464-480d-b38f-3c1134fc51b7">MFPKEY_RESIZE_DST_WIDTH</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c6d47caa-59e1-440c-ab67-955cb8547950">MFPKEY_RESIZE_DST_HEIGHT</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12c26507-c729-4143-a0bd-e043d42744f6">IWMResizerProps Interface</a>
 

 

