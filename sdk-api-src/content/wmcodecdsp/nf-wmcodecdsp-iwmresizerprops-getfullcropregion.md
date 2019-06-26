---
UID: NF:wmcodecdsp.IWMResizerProps.GetFullCropRegion
title: IWMResizerProps::GetFullCropRegion (wmcodecdsp.h)
author: windows-sdk-content
description: Retrieves the source and destination rectangles.
old-location: mf\iwmresizerpropsgetfullcropregion.htm
tech.root: medfound
ms.assetid: 91c37040-a698-489b-95fd-f3088f62e4c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFullCropRegion, GetFullCropRegion method [Media Foundation], GetFullCropRegion method [Media Foundation],IWMResizerProps interface, IWMResizerProps interface [Media Foundation],GetFullCropRegion method, IWMResizerProps.GetFullCropRegion, IWMResizerProps::GetFullCropRegion, codecapi.iwmresizerpropsgetfullcropregion, mf.iwmresizerpropsgetfullcropregion, wmcodecdsp/IWMResizerProps::GetFullCropRegion
ms.topic: method
f1_keywords: 
 - "wmcodecdsp/IWMResizerProps.GetFullCropRegion"
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
 - IWMResizerProps.GetFullCropRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops">IWMResizerProps Interface</a>
 

 

