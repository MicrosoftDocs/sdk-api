---
UID: NF:evr.IEVRTrustedVideoPlugin.IsInTrustedVideoMode
title: IEVRTrustedVideoPlugin::IsInTrustedVideoMode (evr.h)
description: Queries whether the plug-in has any transient vulnerabilities at this time.
helpviewer_keywords: ["43242898-4812-4faa-8e0a-6e60455c9f3b","IEVRTrustedVideoPlugin interface [Media Foundation]","IsInTrustedVideoMode method","IEVRTrustedVideoPlugin.IsInTrustedVideoMode","IEVRTrustedVideoPlugin::IsInTrustedVideoMode","IsInTrustedVideoMode","IsInTrustedVideoMode method [Media Foundation]","IsInTrustedVideoMode method [Media Foundation]","IEVRTrustedVideoPlugin interface","evr/IEVRTrustedVideoPlugin::IsInTrustedVideoMode","mf.ievrtrustedvideoplugin_isintrustedvideomode"]
old-location: mf\ievrtrustedvideoplugin_isintrustedvideomode.htm
tech.root: mfarchive
ms.assetid: 43242898-4812-4faa-8e0a-6e60455c9f3b
ms.date: 12/05/2018
ms.keywords: 43242898-4812-4faa-8e0a-6e60455c9f3b, IEVRTrustedVideoPlugin interface [Media Foundation],IsInTrustedVideoMode method, IEVRTrustedVideoPlugin.IsInTrustedVideoMode, IEVRTrustedVideoPlugin::IsInTrustedVideoMode, IsInTrustedVideoMode, IsInTrustedVideoMode method [Media Foundation], IsInTrustedVideoMode method [Media Foundation],IEVRTrustedVideoPlugin interface, evr/IEVRTrustedVideoPlugin::IsInTrustedVideoMode, mf.ievrtrustedvideoplugin_isintrustedvideomode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRTrustedVideoPlugin::IsInTrustedVideoMode
 - evr/IEVRTrustedVideoPlugin::IsInTrustedVideoMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IEVRTrustedVideoPlugin.IsInTrustedVideoMode
archived: true
---

# IEVRTrustedVideoPlugin::IsInTrustedVideoMode


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Queries whether the plug-in has any transient vulnerabilities at this time.

## -parameters

### -param pYes [out]

Receives a Boolean value. If <b>TRUE</b>, the plug-in has no transient vulnerabilities at the moment and can receive protected content. If <b>FALSE</b>, the plug-in has a transient vulnerability. If the method fails, the EVR treats the value as <b>FALSE</b> (untrusted).

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

This method provides a way for the plug-in to report temporary conditions that would cause the input trust authority (ITA) to distrust the plug-in. For example, if an EVR presenter is in windowed mode, it is vulnerable to GDI screen captures.

To disable screen capture in Direct3D, the plug-in must do the following:

<ul>
<li>
Create the Direct3D device in full-screen exclusive mode.

</li>
<li>
Specify the D3DCREATE_DISABLE_PRINTSCREEN flag when you create the device. For more information, see <b>IDirect3D9::CreateDevice</b> in the DirectX documentation.

</li>
</ul>
In addition, the graphics adapter must support the Windows Vista Display Driver Model (WDDM) and the Direct3D extensions for Windows Vista (sometimes called D3D9Ex or D3D9L).

If these conditions are met, the presenter can return <b>TRUE</b> in the <i>pYes</i> parameter. Otherwise, it should return <b>FALSE</b>.

The EVR calls this method whenever the device changes. If the plug-in returns <b>FALSE</b>, the EVR treats this condition as if the plug-in had a new output connector of unknown type. The policy object can then allow or block playback, depending on the ITA's policy.

This method should be used only to report transient conditions. A plug-in that is never in a trusted state should not implement the <a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin">IEVRTrustedVideoPlugin</a> interface at all.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin">IEVRTrustedVideoPlugin</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>