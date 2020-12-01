---
UID: NF:evr.IMFVideoDisplayControl.GetAspectRatioMode
title: IMFVideoDisplayControl::GetAspectRatioMode (evr.h)
description: Queries how the enhanced video renderer (EVR) handles the aspect ratio of the source video.
helpviewer_keywords: ["GetAspectRatioMode","GetAspectRatioMode method [Media Foundation]","GetAspectRatioMode method [Media Foundation]","IMFVideoDisplayControl interface","IMFVideoDisplayControl interface [Media Foundation]","GetAspectRatioMode method","IMFVideoDisplayControl.GetAspectRatioMode","IMFVideoDisplayControl::GetAspectRatioMode","b5e81f80-e5c9-4ecf-8f10-d52a0533f086","evr/IMFVideoDisplayControl::GetAspectRatioMode","mf.imfvideodisplaycontrol_getaspectratiomode"]
old-location: mf\imfvideodisplaycontrol_getaspectratiomode.htm
tech.root: mf
ms.assetid: b5e81f80-e5c9-4ecf-8f10-d52a0533f086
ms.date: 12/05/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [Media Foundation], GetAspectRatioMode method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetAspectRatioMode method, IMFVideoDisplayControl.GetAspectRatioMode, IMFVideoDisplayControl::GetAspectRatioMode, b5e81f80-e5c9-4ecf-8f10-d52a0533f086, evr/IMFVideoDisplayControl::GetAspectRatioMode, mf.imfvideodisplaycontrol_getaspectratiomode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoDisplayControl::GetAspectRatioMode
 - evr/IMFVideoDisplayControl::GetAspectRatioMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl.GetAspectRatioMode
---

# IMFVideoDisplayControl::GetAspectRatioMode


## -description

Queries how the enhanced video renderer (EVR) handles the aspect ratio of the source video.

## -parameters

### -param pdwAspectRatioMode [out]

Receives a bitwise <b>OR</b> of one or more flags from the <a href="/windows/desktop/api/evr/ne-evr-mfvideoaspectratiomode">MFVideoAspectRatioMode</a> enumeration.

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

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>