---
UID: NF:mfmediaengine.IMFMediaEngineClassFactory.CreateInstance
title: IMFMediaEngineClassFactory::CreateInstance (mfmediaengine.h)
description: Creates a new instance of the Media Engine.
helpviewer_keywords: ["CreateInstance","CreateInstance method [Media Foundation]","CreateInstance method [Media Foundation]","IMFMediaEngineClassFactory interface","IMFMediaEngineClassFactory interface [Media Foundation]","CreateInstance method","IMFMediaEngineClassFactory.CreateInstance","IMFMediaEngineClassFactory::CreateInstance","mf.imfmediaengineclassfactory_createinstance","mfmediaengine/IMFMediaEngineClassFactory::CreateInstance"]
old-location: mf\imfmediaengineclassfactory_createinstance.htm
tech.root: mf
ms.assetid: EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFMediaEngineClassFactory interface, IMFMediaEngineClassFactory interface [Media Foundation],CreateInstance method, IMFMediaEngineClassFactory.CreateInstance, IMFMediaEngineClassFactory::CreateInstance, mf.imfmediaengineclassfactory_createinstance, mfmediaengine/IMFMediaEngineClassFactory::CreateInstance
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaEngineClassFactory::CreateInstance
 - mfmediaengine/IMFMediaEngineClassFactory::CreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineClassFactory.CreateInstance
---

# IMFMediaEngineClassFactory::CreateInstance


## -description

Creates a new instance of the Media Engine.

## -parameters

### -param dwFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_createflags">MF_MEDIA_ENGINE_CREATEFLAGS</a> enumeration.

### -param pAttr [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store. 

This parameter  specifies configuration attributes for the Media Engine. Call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a> to create the attribute store. Then, set one or more attributes from the list of <a href="/windows/desktop/medfound/media-engine-attributes">Media Engine Attributes</a>. For details, see Remarks.

### -param ppPlayer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a> interface. The caller must release the interface.

## -returns

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
A required attribute was missing from <i>pAttr</i>, or an invalid combination of attributes was used.

</td>
</tr>
</table>

## -remarks

Before calling this method, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a>.

The Media Engine supports three distinct modes:

<table>
<tr>
<th>Mode</th>
<th>Description</th>
</tr>
<tr>
<td>Frame-server mode</td>
<td>
In this mode, the Media Engine delivers uncompressed video frames to the application. The application is responsible for displaying each frame, using Microsoft Direct3D or any other rendering technique. 

The Media Engine renders the audio; the application is not responsible for audio rendering.

Frame-server mode is the default mode. 

</td>
</tr>
<tr>
<td>Rendering mode</td>
<td>
In this mode, the Media Engine renders both audio and video. The video is rendered to a window or Microsoft DirectComposition visual provided by the application.

To enable rendering mode, set either the <a href="/windows/desktop/medfound/mf-media-engine-playback-hwnd">MF_MEDIA_ENGINE_PLAYBACK_HWND</a> attribute or the  <a href="/windows/desktop/medfound/mf-media-engine-playback-visual">MF_MEDIA_ENGINE_PLAYBACK_VISUAL</a> attribute.

</td>
</tr>
<tr>
<td>Audio  mode</td>
<td>
In this mode, the Media Engine renders audio only, with no video.

To enable audio mode, set the <b>MF_MEDIA_ENGINE_AUDIOONLY</b> flag in the <i>dwFlags</i> parameter.

</td>
</tr>
</table>
 

<h3><a id="Intialization_Attributes"></a><a id="intialization_attributes"></a><a id="INTIALIZATION_ATTRIBUTES"></a>Initialization Attributes</h3>
The following attributes are defined for the <i>pAttr</i> parameter. Some are required, and some are optional, depending on the  mode you want. 

<table>
<tr>
<th>Feature</th>
<th>Attributes</th>
<th>Frame Server Mode</th>
<th>Rendering Mode</th>
<th>Audio Mode</th>
</tr>
<tr>
<td>Event callback</td>
<td>
<a href="/windows/desktop/medfound/mf-media-engine-callback">MF_MEDIA_ENGINE_CALLBACK</a>
</td>
<td>Required.</td>
<td>Required.</td>
<td>Required.</td>
</tr>
<tr>
<td>Render target</td>
<td>
One of the following:

<dl>
<dd>
<a href="/windows/desktop/medfound/mf-media-engine-playback-hwnd">MF_MEDIA_ENGINE_PLAYBACK_HWND</a>
</dd>
<dd>
<a href="/windows/desktop/medfound/mf-media-engine-playback-visual">MF_MEDIA_ENGINE_PLAYBACK_VISUAL</a>
</dd>
</dl>
These attributes are mutually exclusive. Setting either of these attributes puts the Media Engine into rendering mode.

</td>
<td>Do not set.</td>
<td>Required. </td>
<td>Do not set.</td>
</tr>
<tr>
<td>Direct3D format</td>
<td>
<a href="/windows/desktop/medfound/mf-media-engine-video-output-format">MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT</a>
</td>
<td>Required.</td>
<td>Optional.</td>
<td>Do not set.</td>
</tr>
<tr>
<td>Microsoft DirectX Graphics Infrastructure (DXGI) device  manager</td>
<td>
<a href="/windows/desktop/medfound/mf-media-engine-dxgi-manager">MF_MEDIA_ENGINE_DXGI_MANAGER</a>
</td>
<td>Optional.</td>
<td>Optional.</td>
<td>Do not set.</td>
</tr>
<tr>
<td>Media Engine extensions</td>
<td>
<a href="/windows/desktop/medfound/mf-media-engine-extension">MF_MEDIA_ENGINE_EXTENSION</a>
</td>
<td>Optional.</td>
<td>Optional.</td>
<td>Optional.</td>
</tr>
<tr>
<td>Content protection</td>
<td>
Any of the following:

<dl>
<dd>
<a href="/windows/desktop/medfound/mf-media-engine-opm-hwnd">MF_MEDIA_ENGINE_OPM_HWND</a>
</dd>
<dd>
<a href="/windows/desktop/medfound/mf-media-engine-content-protection-flags">MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS</a>
</dd>
<dd>
<a href="/windows/desktop/medfound/mf-media-engine-content-protection-manager">MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER</a>
</dd>
</dl>
</td>
<td>Optional.</td>
<td>Optional.</td>
<td>Optional.</td>
</tr>
<tr>
<td>Audio playback</td>
<td>
Any of the following:

<dl>
<dd>
<a href="/windows/desktop/medfound/mf-media-engine-audio-category">MF_MEDIA_ENGINE_AUDIO_CATEGORY</a>
</dd>
<dd>
<a href="/windows/desktop/medfound/mf-media-engine-audio-endpoint-role">MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE</a>
</dd>
</dl>
</td>
<td>Optional.</td>
<td>Optional.</td>
<td>Optional.</td>
</tr>
</table>
 

<h3><a id="Windows_Phone_8"></a><a id="windows_phone_8"></a><a id="WINDOWS_PHONE_8"></a>Windows Phone 8</h3>
 This API is supported.

On the phone, the Media Engine only supports frame-server mode. Attempting to initialize the interface in either rendering mode or audio mode will fail.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory">IMFMediaEngineClassFactory</a>