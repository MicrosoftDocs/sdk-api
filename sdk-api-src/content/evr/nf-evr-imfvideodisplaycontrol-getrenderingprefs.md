---
UID: NF:evr.IMFVideoDisplayControl.GetRenderingPrefs
title: IMFVideoDisplayControl::GetRenderingPrefs (evr.h)
description: Gets various video rendering settings.helpviewer_keywords: ["9a5bd1d6-e604-4798-af29-ad0c1931b651","GetRenderingPrefs","GetRenderingPrefs method [Media Foundation]","GetRenderingPrefs method [Media Foundation]","IMFVideoDisplayControl interface","IMFVideoDisplayControl interface [Media Foundation]","GetRenderingPrefs method","IMFVideoDisplayControl.GetRenderingPrefs","IMFVideoDisplayControl::GetRenderingPrefs","evr/IMFVideoDisplayControl::GetRenderingPrefs","mf.imfvideodisplaycontrol_getrenderingprefs"]
old-location: mf\imfvideodisplaycontrol_getrenderingprefs.htm
tech.root: medfound
ms.assetid: 9a5bd1d6-e604-4798-af29-ad0c1931b651
ms.date: 12/05/2018
ms.keywords: 9a5bd1d6-e604-4798-af29-ad0c1931b651, GetRenderingPrefs, GetRenderingPrefs method [Media Foundation], GetRenderingPrefs method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetRenderingPrefs method, IMFVideoDisplayControl.GetRenderingPrefs, IMFVideoDisplayControl::GetRenderingPrefs, evr/IMFVideoDisplayControl::GetRenderingPrefs, mf.imfvideodisplaycontrol_getrenderingprefs
f1_keywords:
- evr/IMFVideoDisplayControl.GetRenderingPrefs
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
- IMFVideoDisplayControl.GetRenderingPrefs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl::GetRenderingPrefs


## -description


Gets various video rendering settings.
        


## -parameters




### -param pdwRenderFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/evr/ne-evr-mfvideorenderprefs">MFVideoRenderPrefs</a> enumeration.


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




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

