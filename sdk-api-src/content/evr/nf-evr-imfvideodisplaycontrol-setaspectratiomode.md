---
UID: NF:evr.IMFVideoDisplayControl.SetAspectRatioMode
title: IMFVideoDisplayControl::SetAspectRatioMode
author: windows-sdk-content
description: Specifies how the enhanced video renderer (EVR) handles the aspect ratio of the source video.
old-location: mf\imfvideodisplaycontrol_setaspectratiomode.htm
old-project: medfound
ms.assetid: dd49a110-1c11-4eca-9e7b-6021f3bdd397
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFVideoDisplayControl interface [Media Foundation],SetAspectRatioMode method, IMFVideoDisplayControl.SetAspectRatioMode, IMFVideoDisplayControl::SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [Media Foundation], SetAspectRatioMode method [Media Foundation],IMFVideoDisplayControl interface, dd49a110-1c11-4eca-9e7b-6021f3bdd397, evr/IMFVideoDisplayControl::SetAspectRatioMode, mf.imfvideodisplaycontrol_setaspectratiomode
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
 - IMFVideoDisplayControl.SetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDisplayControl::SetAspectRatioMode


## -description



Specifies how the enhanced video renderer (EVR) handles the aspect ratio of the source video.




## -parameters




### -param dwAspectRatioMode [in]

Bitwise <b>OR</b> of one or more flags from the <a href="https://msdn.microsoft.com/c0a34cff-f86f-4005-9320-5dadfdde5808">MFVideoAspectRatioMode</a> enumeration.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid flags.

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
 

 

