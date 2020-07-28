---
UID: NF:evr.IMFVideoDisplayControl.SetRenderingPrefs
title: IMFVideoDisplayControl::SetRenderingPrefs (evr.h)
description: Sets various preferences related to video rendering.
helpviewer_keywords: ["7603aaf8-1671-4b35-bee5-335f656de3c5","IMFVideoDisplayControl interface [Media Foundation]","SetRenderingPrefs method","IMFVideoDisplayControl.SetRenderingPrefs","IMFVideoDisplayControl::SetRenderingPrefs","SetRenderingPrefs","SetRenderingPrefs method [Media Foundation]","SetRenderingPrefs method [Media Foundation]","IMFVideoDisplayControl interface","evr/IMFVideoDisplayControl::SetRenderingPrefs","mf.imfvideodisplaycontrol_setrenderingprefs"]
old-location: mf\imfvideodisplaycontrol_setrenderingprefs.htm
tech.root: mf
ms.assetid: 7603aaf8-1671-4b35-bee5-335f656de3c5
ms.date: 12/05/2018
ms.keywords: 7603aaf8-1671-4b35-bee5-335f656de3c5, IMFVideoDisplayControl interface [Media Foundation],SetRenderingPrefs method, IMFVideoDisplayControl.SetRenderingPrefs, IMFVideoDisplayControl::SetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [Media Foundation], SetRenderingPrefs method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetRenderingPrefs, mf.imfvideodisplaycontrol_setrenderingprefs
f1_keywords:
- evr/IMFVideoDisplayControl.SetRenderingPrefs
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
- IMFVideoDisplayControl.SetRenderingPrefs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl::SetRenderingPrefs


## -description



Sets various preferences related to video rendering.




## -parameters




### -param dwRenderFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/evr/ne-evr-mfvideorenderprefs">MFVideoRenderPrefs</a> enumeration.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

