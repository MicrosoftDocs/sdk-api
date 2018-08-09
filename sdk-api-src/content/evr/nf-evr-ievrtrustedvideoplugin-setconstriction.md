---
UID: NF:evr.IEVRTrustedVideoPlugin.SetConstriction
title: IEVRTrustedVideoPlugin::SetConstriction
author: windows-sdk-content
description: Limits the effective video resolution.
old-location: mf\ievrtrustedvideoplugin_setconstriction.htm
old-project: medfound
ms.assetid: f2e9b199-969f-453c-8714-fa85c89a191a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IEVRTrustedVideoPlugin interface [Media Foundation],SetConstriction method, IEVRTrustedVideoPlugin.SetConstriction, IEVRTrustedVideoPlugin::SetConstriction, SetConstriction, SetConstriction method [Media Foundation], SetConstriction method [Media Foundation],IEVRTrustedVideoPlugin interface, evr/IEVRTrustedVideoPlugin::SetConstriction, f2e9b199-969f-453c-8714-fa85c89a191a, mf.ievrtrustedvideoplugin_setconstriction
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
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IEVRTrustedVideoPlugin.SetConstriction
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEVRTrustedVideoPlugin::SetConstriction


## -description


Limits the effective video resolution.
        


## -parameters




### -param dwKPix [in]

Maximum number of source pixels that may appear in the final video image, in thousands of pixels. If the value is zero, the video is disabled. If the value is MAXDWORD (0xFFFFFFFF), video constriction is removed and the video may be rendered at full resolution.


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



This method limits the effective resolution of the video image. The actual resolution on the target device might be higher, due to stretching the image.

The EVR might call this method at any time if the <a href="https://msdn.microsoft.com/16bb31c3-51f7-4d9b-946c-f366fb6e5dee">IEVRTrustedVideoPlugin::CanConstrict</a> method returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/1dcaa01c-2596-4a22-9e2a-7f0e26d58ffe">IEVRTrustedVideoPlugin</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

