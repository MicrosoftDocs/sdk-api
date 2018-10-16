---
UID: NF:evr.IMFVideoDisplayControl.GetVideoPosition
title: IMFVideoDisplayControl::GetVideoPosition
author: windows-sdk-content
description: Gets the source and destination rectangles for the video.
old-location: mf\imfvideodisplaycontrol_getvideoposition.htm
tech.root: medfound
ms.assetid: 59c2e914-cc15-4534-976c-a760ff97f6ae
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 59c2e914-cc15-4534-976c-a760ff97f6ae, GetVideoPosition, GetVideoPosition method [Media Foundation], GetVideoPosition method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetVideoPosition method, IMFVideoDisplayControl.GetVideoPosition, IMFVideoDisplayControl::GetVideoPosition, evr/IMFVideoDisplayControl::GetVideoPosition, mf.imfvideodisplaycontrol_getvideoposition
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
 - IMFVideoDisplayControl.GetVideoPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoDisplayControl::GetVideoPosition


## -description


Gets the source and destination rectangles for the video.
        


## -parameters




### -param pnrcSource [out]

Pointer to an <a href="https://msdn.microsoft.com/c1dd42ca-64a0-4f30-82e1-eda3f4721526">MFVideoNormalizedRect</a> structure that receives the source rectangle.


### -param prcDest [out]

Receives the current destination rectangle.


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
One or more required parameters are <b>NULL</b>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

