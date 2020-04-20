---
UID: NF:evr.IEVRTrustedVideoPlugin.CanConstrict
title: IEVRTrustedVideoPlugin::CanConstrict (evr.h)
description: Queries whether the plug-in can limit the effective video resolution.helpviewer_keywords: ["16bb31c3-51f7-4d9b-946c-f366fb6e5dee","CanConstrict","CanConstrict method [Media Foundation]","CanConstrict method [Media Foundation]","IEVRTrustedVideoPlugin interface","IEVRTrustedVideoPlugin interface [Media Foundation]","CanConstrict method","IEVRTrustedVideoPlugin.CanConstrict","IEVRTrustedVideoPlugin::CanConstrict","evr/IEVRTrustedVideoPlugin::CanConstrict","mf.ievrtrustedvideoplugin_canconstrict"]
old-location: mf\ievrtrustedvideoplugin_canconstrict.htm
tech.root: medfound
ms.assetid: 16bb31c3-51f7-4d9b-946c-f366fb6e5dee
ms.date: 12/05/2018
ms.keywords: 16bb31c3-51f7-4d9b-946c-f366fb6e5dee, CanConstrict, CanConstrict method [Media Foundation], CanConstrict method [Media Foundation],IEVRTrustedVideoPlugin interface, IEVRTrustedVideoPlugin interface [Media Foundation],CanConstrict method, IEVRTrustedVideoPlugin.CanConstrict, IEVRTrustedVideoPlugin::CanConstrict, evr/IEVRTrustedVideoPlugin::CanConstrict, mf.ievrtrustedvideoplugin_canconstrict
f1_keywords:
- evr/IEVRTrustedVideoPlugin.CanConstrict
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
- IEVRTrustedVideoPlugin.CanConstrict
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEVRTrustedVideoPlugin::CanConstrict


## -description


Queries whether the plug-in can limit the effective video resolution.
        


## -parameters




### -param pYes [out]

Receives a Boolean value. If <b>TRUE</b>, the plug-in can limit the effective video resolution. Otherwise, the plug-in cannot limit the video resolution. If the method fails, the EVR treats the value as <b>FALSE</b> (not supported).


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



Constriction is a protection mechanism that limits the effective resolution of the video frame to a specified maximum number of pixels.

Video constriction can be implemented by either the mixer or the presenter.

If the method returns <b>TRUE</b>, the EVR might call <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-ievrtrustedvideoplugin-setconstriction">IEVRTrustedVideoPlugin::SetConstriction</a> at any time.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin">IEVRTrustedVideoPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 

