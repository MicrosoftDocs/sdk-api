---
UID: NF:mfmediaengine.IMFMediaEngineClassFactory.CreateInstance
title: IMFMediaEngineClassFactory::CreateInstance
author: windows-sdk-content
description: Creates a new instance of the Media Engine.
old-location: mf\imfmediaengineclassfactory_createinstance.htm
tech.root: medfound
ms.assetid: EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFMediaEngineClassFactory interface, IMFMediaEngineClassFactory interface [Media Foundation],CreateInstance method, IMFMediaEngineClassFactory.CreateInstance, IMFMediaEngineClassFactory::CreateInstance, mf.imfmediaengineclassfactory_createinstance, mfmediaengine/IMFMediaEngineClassFactory::CreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineClassFactory.CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineClassFactory::CreateInstance


## -description


Creates a new instance of the Media Engine.


## -parameters




### -param dwFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/1709B08C-D4DC-4A33-9B92-1C4961208684">MF_MEDIA_ENGINE_CREATEFLAGS</a> enumeration.


### -param pAttr [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store. 

This parameter  specifies configuration attributes for the Media Engine. Call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a> to create the attribute store. Then, set one or more attributes from the list of <a href="https://msdn.microsoft.com/08282D80-53F5-463F-B87F-522F72823E99">Media Engine Attributes</a>. For details, see Remarks.


### -param ppPlayer [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a> interface. The caller must release the interface.


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



Before calling this method, call <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a>.

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

To enable rendering mode, set either the <a href="https://msdn.microsoft.com/63889D81-12C5-47C1-B52A-6358E68830C3">MF_MEDIA_ENGINE_PLAYBACK_HWND</a> attribute or the  <a href="https://msdn.microsoft.com/C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633">MF_MEDIA_ENGINE_PLAYBACK_VISUAL</a> attribute.

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
 

<h3><a id="Intialization_Attributes"></a><a id="intialization_attributes"></a><a id="INTIALIZATION_ATTRIBUTES"></a>Intialization Attributes</h3>
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
<a href="https://msdn.microsoft.com/5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D">MF_MEDIA_ENGINE_CALLBACK</a>
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
<a href="https://msdn.microsoft.com/63889D81-12C5-47C1-B52A-6358E68830C3">MF_MEDIA_ENGINE_PLAYBACK_HWND</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633">MF_MEDIA_ENGINE_PLAYBACK_VISUAL</a>
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
<a href="https://msdn.microsoft.com/70FFDD44-9FDE-4D86-AD65-60019AC4A2BC">MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT</a>
</td>
<td>Required.</td>
<td>Optional.</td>
<td>Do not set.</td>
</tr>
<tr>
<td>Microsoft DirectX Graphics Infrastructure (DXGI) device  manager</td>
<td>
<a href="https://msdn.microsoft.com/CB952492-0ACF-4501-BD8B-133E26FCE8F7">MF_MEDIA_ENGINE_DXGI_MANAGER</a>
</td>
<td>Optional.</td>
<td>Optional.</td>
<td>Do not set.</td>
</tr>
<tr>
<td>Media Engine extensions</td>
<td>
<a href="https://msdn.microsoft.com/D2F3F41D-086A-4DEB-99D0-07574BC8F0D7">MF_MEDIA_ENGINE_EXTENSION</a>
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
<a href="https://msdn.microsoft.com/E5271D72-FE16-4D28-9BBA-1440C7CE0921">MF_MEDIA_ENGINE_OPM_HWND</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/2A593499-BF40-440E-AF1D-3B0E7732489A">MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/F6F17EC7-6553-4127-B691-C20C945DD4D8">MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER</a>
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
<a href="https://msdn.microsoft.com/0F2DB9A7-64ED-4952-BCB3-F2B15BA37D2A">MF_MEDIA_ENGINE_AUDIO_CATEGORY</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/E4B7660D-5F41-495A-B77D-94B7981F4C2C">MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE</a>
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




<a href="https://msdn.microsoft.com/8E4E84A0-BCFC-4CBF-813B-4FEE2B42A83E">IMFMediaEngineClassFactory</a>
 

 

