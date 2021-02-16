---
UID: NF:amvideo.IFullScreenVideoEx.SetEnabled
title: IFullScreenVideoEx::SetEnabled (amvideo.h)
description: The SetEnabled method enables or disables a specified display mode.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetEnabled method","IFullScreenVideoEx.SetEnabled","IFullScreenVideoEx::SetEnabled","IFullScreenVideoSetEnabled","OAFALSE","OATRUE","SetEnabled","SetEnabled method [DirectShow]","SetEnabled method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetEnabled","dshow.ifullscreenvideoex_setenabled"]
old-location: dshow\ifullscreenvideoex_setenabled.htm
tech.root: dshow
ms.assetid: f05c1b3e-3ebc-4753-b3ca-e52907c59121
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetEnabled method, IFullScreenVideoEx.SetEnabled, IFullScreenVideoEx::SetEnabled, IFullScreenVideoSetEnabled, OAFALSE, OATRUE, SetEnabled, SetEnabled method [DirectShow], SetEnabled method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetEnabled, dshow.ifullscreenvideoex_setenabled
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IFullScreenVideoEx::SetEnabled
 - amvideo/IFullScreenVideoEx::SetEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.SetEnabled
---

# IFullScreenVideoEx::SetEnabled


## -description

The <code>SetEnabled</code> method enables or disables a specified display mode.

## -parameters

### -param Mode [in]

Index of the display mode to enable or disable.

### -param bEnabled [in]

Specifies one of the following Boolean values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OATRUE"></a><a id="oatrue"></a><dl>
<dt><b>OATRUE</b></dt>
</dl>
</td>
<td width="60%">
Enable the specified display mode.

</td>
</tr>
<tr>
<td width="40%"><a id="OAFALSE"></a><a id="oafalse"></a><dl>
<dt><b>OAFALSE</b></dt>
</dl>
</td>
<td width="60%">
Disable the specified display mode.

</td>
</tr>
</table>

## -returns

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
</table>

## -remarks

The Full Screen Renderer supports a static set of display modes. By default, every mode is enabled. You can use this method to enable or disable a particular display mode. The video card on the user's system might not support every mode. The Full Screen Renderer will not use a mode that the video card does not support, even if that mode is enabled. To determine whether the card supports a particular mode, call the <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable">IFullScreenVideoEx::IsModeAvailable</a> method. If a mode is disabled, the Full Screen Renderer will not use it, even if the card supports it.

Display modes are indexed from zero. The <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-countmodes">IFullScreenVideoEx::CountModes</a> method returns the number of modes. To retrieve the width, height, and bit depth of a particular display mode, call the <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo">IFullScreenVideoEx::GetModeInfo</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>