---
UID: NF:evr9.IMFVideoProcessor.SetBackgroundColor
title: IMFVideoProcessor::SetBackgroundColor (evr9.h)
description: Sets the background color for the composition rectangle. The background color is used for letterboxing the video image.
helpviewer_keywords: ["IMFVideoProcessor interface [Media Foundation]","SetBackgroundColor method","IMFVideoProcessor.SetBackgroundColor","IMFVideoProcessor::SetBackgroundColor","SetBackgroundColor","SetBackgroundColor method [Media Foundation]","SetBackgroundColor method [Media Foundation]","IMFVideoProcessor interface","evr9/IMFVideoProcessor::SetBackgroundColor","fb654dba-1f03-48a7-ac8e-fa0c82f29849","mf.imfvideoprocessor_setbackgroundcolor"]
old-location: mf\imfvideoprocessor_setbackgroundcolor.htm
tech.root: mf
ms.assetid: fb654dba-1f03-48a7-ac8e-fa0c82f29849
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessor interface [Media Foundation],SetBackgroundColor method, IMFVideoProcessor.SetBackgroundColor, IMFVideoProcessor::SetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [Media Foundation], SetBackgroundColor method [Media Foundation],IMFVideoProcessor interface, evr9/IMFVideoProcessor::SetBackgroundColor, fb654dba-1f03-48a7-ac8e-fa0c82f29849, mf.imfvideoprocessor_setbackgroundcolor
f1_keywords:
- evr9/IMFVideoProcessor.SetBackgroundColor
dev_langs:
- c++
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
api_name:
- IMFVideoProcessor.SetBackgroundColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoProcessor::SetBackgroundColor


## -description



Sets the background color for the composition rectangle. The background color is used for letterboxing the video image.




## -parameters




### -param ClrBkg [in]

Background color, specified as a <b>COLORREF</b> value. Use the <b>RGB</b> macro to create this value.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>
 

 

