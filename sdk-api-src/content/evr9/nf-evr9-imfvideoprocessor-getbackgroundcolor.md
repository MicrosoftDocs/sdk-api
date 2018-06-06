---
UID: NF:evr9.IMFVideoProcessor.GetBackgroundColor
title: IMFVideoProcessor::GetBackgroundColor
author: windows-sdk-content
description: Retrieves the background color for the composition rectangle. The background color is used for letterboxing the video image.
old-location: mf\imfvideoprocessor_getbackgroundcolor.htm
old-project: medfound
ms.assetid: d9068346-f0b3-4361-a56b-2360ecc3b9d9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [Media Foundation], GetBackgroundColor method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetBackgroundColor method, IMFVideoProcessor.GetBackgroundColor, IMFVideoProcessor::GetBackgroundColor, d9068346-f0b3-4361-a56b-2360ecc3b9d9, evr9/IMFVideoProcessor::GetBackgroundColor, mf.imfvideoprocessor_getbackgroundcolor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFVideoAlphaBitmapFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoProcessor.GetBackgroundColor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoProcessor::GetBackgroundColor


## -description



Retrieves the background color for the composition rectangle. The background color is used for letterboxing the video image.




## -parameters




### -param lpClrBkg [out]

Pointer to a <b>COLORREF</b> value that receives the background color.


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




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/0a63c4f8-eb32-4f0c-b69b-0c16243f2f21">IMFVideoProcessor</a>
 

 

