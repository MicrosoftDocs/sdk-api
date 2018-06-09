---
UID: NF:evr.IMFVideoDisplayControl.SetVideoPosition
title: IMFVideoDisplayControl::SetVideoPosition
author: windows-sdk-content
description: Sets the source and destination rectangles for the video.
old-location: mf\imfvideodisplaycontrol_setvideoposition.htm
old-project: medfound
ms.assetid: 5dc789b7-e206-4f1d-a0b2-12cb98ce4184
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: 5dc789b7-e206-4f1d-a0b2-12cb98ce4184, IMFVideoDisplayControl interface [Media Foundation],SetVideoPosition method, IMFVideoDisplayControl.SetVideoPosition, IMFVideoDisplayControl::SetVideoPosition, SetVideoPosition, SetVideoPosition method [Media Foundation], SetVideoPosition method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetVideoPosition, mf.imfvideodisplaycontrol_setvideoposition
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl.SetVideoPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::SetVideoPosition


## -description



Sets the source and destination rectangles for the video.




## -parameters




### -param pnrcSource [in]

Pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that specifies the source rectangle. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the source rectangle does not change.


### -param prcDest [in]

Specifies the destination rectangle. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the destination rectangle does not change.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter must be non-<b>NULL</b>.

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



The source rectangle defines which portion of the video is displayed. It is specified in <i>normalized</i> coordinates. For more information, see <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure. To display the entire video image, set the source rectangle to {0, 0, 1, 1}. The default source rectangle is {0, 0, 1, 1}.

The destination rectangle defines a rectangle within the clipping window where the video appears. It is specified in pixels, relative to the client area of the window. To fill the entire window, set the destination rectangle to {0, 0, <i>width</i>, <i>height</i>}, where <i>width</i> and <i>height</i> are dimensions of the window client area. The default destination rectangle is {0, 0, 0, 0}.

To update just one of these rectangles, set the other parameter to <b>NULL</b>. You can set <i>pnrcSource</i> or <i>prcDest</i> to <b>NULL</b>, but not both.

Before setting the destination rectangle (<i>prcDest</i>), you must set the video window by calling <a href="https://msdn.microsoft.com/50bc345c-ee44-4174-9b1a-e406041096b5">IMFVideoDisplayControl::SetVideoWindow</a>. (For the Media Foundation version of the EVR, you can also provide the video window in the <a href="https://msdn.microsoft.com/021887fc-36af-42d4-ae46-2edc1c700110">MFCreateVideoRendererActivate</a> function.) If no video window was provided, <b>SetVideoPosition</b> returns E_POINTER.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

