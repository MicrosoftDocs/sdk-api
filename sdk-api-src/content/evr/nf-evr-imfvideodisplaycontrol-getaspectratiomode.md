---
UID: NF:evr.IMFVideoDisplayControl.GetAspectRatioMode
title: IMFVideoDisplayControl::GetAspectRatioMode
author: windows-driver-content
description: Queries how the enhanced video renderer (EVR) handles the aspect ratio of the source video.
old-location: mf\imfvideodisplaycontrol_getaspectratiomode.htm
old-project: medfound
ms.assetid: b5e81f80-e5c9-4ecf-8f10-d52a0533f086
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [Media Foundation], GetAspectRatioMode method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetAspectRatioMode method, IMFVideoDisplayControl.GetAspectRatioMode, IMFVideoDisplayControl::GetAspectRatioMode, b5e81f80-e5c9-4ecf-8f10-d52a0533f086, evr/IMFVideoDisplayControl::GetAspectRatioMode, mf.imfvideodisplaycontrol_getaspectratiomode
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
-	IMFVideoDisplayControl.GetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::GetAspectRatioMode


## -description



          Queries how the enhanced video renderer (EVR) handles the aspect ratio of the source video.
        


## -parameters




### -param pdwAspectRatioMode [out]

Receives a bitwise <b>OR</b> of one or more flags from the <a href="https://msdn.microsoft.com/c0a34cff-f86f-4005-9320-5dadfdde5808">MFVideoAspectRatioMode</a> enumeration.


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
 




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

