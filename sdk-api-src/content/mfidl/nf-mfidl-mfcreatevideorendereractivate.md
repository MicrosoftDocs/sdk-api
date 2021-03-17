---
UID: NF:mfidl.MFCreateVideoRendererActivate
title: MFCreateVideoRendererActivate function (mfidl.h)
description: Creates an activation object for the enhanced video renderer (EVR) media sink.
helpviewer_keywords: ["021887fc-36af-42d4-ae46-2edc1c700110","MFCreateVideoRendererActivate","MFCreateVideoRendererActivate function [Media Foundation]","mf.mfcreatevideorendereractivate","mfidl/MFCreateVideoRendererActivate"]
old-location: mf\mfcreatevideorendereractivate.htm
tech.root: mf
ms.assetid: 021887fc-36af-42d4-ae46-2edc1c700110
ms.date: 12/05/2018
ms.keywords: 021887fc-36af-42d4-ae46-2edc1c700110, MFCreateVideoRendererActivate, MFCreateVideoRendererActivate function [Media Foundation], mf.mfcreatevideorendereractivate, mfidl/MFCreateVideoRendererActivate
req.header: mfidl.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateVideoRendererActivate
 - mfidl/MFCreateVideoRendererActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateVideoRendererActivate
---

# MFCreateVideoRendererActivate function


## -description

Creates an activation object for the enhanced video renderer (EVR) media sink.

## -parameters

### -param hwndVideo [in]

Handle to the window where the video will be displayed.

### -param ppActivate [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. Use this interface to create the EVR. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

To create the EVR, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> on the retrieved <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer. (If you are using the Media Session, the Media Session automatically calls <b>ActivateObject</b> when you queue the topology.)

To configure the EVR, set any of the following attributes on the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object before calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a>.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-activate-custom-video-mixer-activate-attribute">MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE</a>
</td>
<td>Activation object for a custom mixer.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-activate-custom-video-mixer-clsid-attribute">MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID</a>
</td>
<td>CLSID for a custom mixer.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-activate-custom-video-mixer-flags-attribute">MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS</a>
</td>
<td>Flags for creating a custom mixer.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-activate-custom-video-presenter-activate-attribute">MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE</a>
</td>
<td>Activation object for a custom presenter.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-activate-custom-video-presenter-clsid-attribute">MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID</a>
</td>
<td>CLSID for a custom presenter.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mf-activate-custom-video-presenter-flags-attribute">MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS</a>
</td>
<td>Flags for creating a custom presenter.</td>
</tr>
</table>
 

When <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> is called, the activation objects sets the video window on the EVR by calling <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition">IMFVideoDisplayControl::SetVideoPosition</a>. Passing <b>NULL</b> for the <i>hwndVideo</i> parameter is not an error, but no video will render unless the EVR has a valid video window.

## -see-also

<a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>