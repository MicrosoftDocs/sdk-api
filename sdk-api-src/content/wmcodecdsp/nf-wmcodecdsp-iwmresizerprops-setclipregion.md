---
UID: NF:wmcodecdsp.IWMResizerProps.SetClipRegion
title: IWMResizerProps::SetClipRegion
author: windows-sdk-content
description: Sets the source rectangle.
old-location: mf\iwmresizerpropssetclipregion.htm
tech.root: medfound
ms.assetid: 51a11e24-a4c3-49fb-86ec-17baa1773caf
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IWMResizerProps interface [Media Foundation],SetClipRegion method, IWMResizerProps.SetClipRegion, IWMResizerProps::SetClipRegion, SetClipRegion, SetClipRegion method [Media Foundation], SetClipRegion method [Media Foundation],IWMResizerProps interface, codecapi.iwmresizerpropssetclipregion, mf.iwmresizerpropssetclipregion, wmcodecdsp/IWMResizerProps::SetClipRegion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMResizerProps.SetClipRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMResizerProps::SetClipRegion


## -description


Sets the source rectangle.



## -parameters




### -param lClipOriXSrc [in]

Specifies the left edge of the source rectangle, in pixels.


### -param lClipOriYSrc [in]

Specifies the top edge of the source rectangle, in pixels.


### -param lClipWidthSrc [in]

Specifies the width of the source rectangle, in pixels.


### -param lClipHeightSrc [in]

Specifies the height of the source rectangle, in pixels.


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



By default, the video resizer copies the entire video frame. When you call this method, the video resizer crops the video to the source rectangle and copies that portion to the output buffer.

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
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12c26507-c729-4143-a0bd-e043d42744f6">IWMResizerProps Interface</a>
 

 

