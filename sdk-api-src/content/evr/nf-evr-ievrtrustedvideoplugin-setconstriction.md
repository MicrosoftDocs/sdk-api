---
UID: NF:evr.IEVRTrustedVideoPlugin.SetConstriction
title: IEVRTrustedVideoPlugin::SetConstriction (evr.h)
description: Limits the effective video resolution.helpviewer_keywords: ["IEVRTrustedVideoPlugin interface [Media Foundation]","SetConstriction method","IEVRTrustedVideoPlugin.SetConstriction","IEVRTrustedVideoPlugin::SetConstriction","SetConstriction","SetConstriction method [Media Foundation]","SetConstriction method [Media Foundation]","IEVRTrustedVideoPlugin interface","evr/IEVRTrustedVideoPlugin::SetConstriction","f2e9b199-969f-453c-8714-fa85c89a191a","mf.ievrtrustedvideoplugin_setconstriction"]
old-location: mf\ievrtrustedvideoplugin_setconstriction.htm
tech.root: medfound
ms.assetid: f2e9b199-969f-453c-8714-fa85c89a191a
ms.date: 12/05/2018
ms.keywords: IEVRTrustedVideoPlugin interface [Media Foundation],SetConstriction method, IEVRTrustedVideoPlugin.SetConstriction, IEVRTrustedVideoPlugin::SetConstriction, SetConstriction, SetConstriction method [Media Foundation], SetConstriction method [Media Foundation],IEVRTrustedVideoPlugin interface, evr/IEVRTrustedVideoPlugin::SetConstriction, f2e9b199-969f-453c-8714-fa85c89a191a, mf.ievrtrustedvideoplugin_setconstriction
f1_keywords:
- evr/IEVRTrustedVideoPlugin.SetConstriction
dev_langs:
- c++
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The EVR might call this method at any time if the <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-ievrtrustedvideoplugin-canconstrict">IEVRTrustedVideoPlugin::CanConstrict</a> method returns <b>TRUE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin">IEVRTrustedVideoPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 

