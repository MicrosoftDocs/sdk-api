---
UID: NF:evr.IMFVideoDisplayControl.GetBorderColor
title: IMFVideoDisplayControl::GetBorderColor
author: windows-driver-content
description: Gets the border color for the video.
old-location: mf\imfvideodisplaycontrol_getbordercolor.htm
old-project: medfound
ms.assetid: 1b65b793-d06d-4d7f-a19f-0068dd7f2e44
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 1b65b793-d06d-4d7f-a19f-0068dd7f2e44, GetBorderColor, GetBorderColor method [Media Foundation], GetBorderColor method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetBorderColor method, IMFVideoDisplayControl.GetBorderColor, IMFVideoDisplayControl::GetBorderColor, evr/IMFVideoDisplayControl::GetBorderColor, mf.imfvideodisplaycontrol_getbordercolor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: evr.h
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
req.typenames: MFVideoMixPrefs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmiids.lib
-	strmiids.dll
api_name:
-	IMFVideoDisplayControl.GetBorderColor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::GetBorderColor


## -description



          Gets the border color for the video.
        


## -parameters




### -param pClr [out]

Receives the border color, as a <b>COLORREF</b> value.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>
 




## -remarks



The border color is used for areas where the enhanced video renderer (EVR) does not draw any video.

The border color is not used for letterboxing. To get the letterbox color, call <a href="https://msdn.microsoft.com/d9068346-f0b3-4361-a56b-2360ecc3b9d9">IMFVideoProcessor::GetBackgroundColor</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

