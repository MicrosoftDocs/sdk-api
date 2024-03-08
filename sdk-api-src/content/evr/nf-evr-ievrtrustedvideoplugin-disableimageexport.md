---
UID: NF:evr.IEVRTrustedVideoPlugin.DisableImageExport
title: IEVRTrustedVideoPlugin::DisableImageExport (evr.h)
description: Enables or disables the ability of the plug-in to export the video image.
helpviewer_keywords: ["DisableImageExport","DisableImageExport method [Media Foundation]","DisableImageExport method [Media Foundation]","IEVRTrustedVideoPlugin interface","IEVRTrustedVideoPlugin interface [Media Foundation]","DisableImageExport method","IEVRTrustedVideoPlugin.DisableImageExport","IEVRTrustedVideoPlugin::DisableImageExport","dd9811f7-7a9f-4b7e-8425-cb25efe0a71d","evr/IEVRTrustedVideoPlugin::DisableImageExport","mf.ievrtrustedvideoplugin_disableimageexport"]
old-location: mf\ievrtrustedvideoplugin_disableimageexport.htm
tech.root: mfarchive
ms.assetid: dd9811f7-7a9f-4b7e-8425-cb25efe0a71d
ms.date: 12/05/2018
ms.keywords: DisableImageExport, DisableImageExport method [Media Foundation], DisableImageExport method [Media Foundation],IEVRTrustedVideoPlugin interface, IEVRTrustedVideoPlugin interface [Media Foundation],DisableImageExport method, IEVRTrustedVideoPlugin.DisableImageExport, IEVRTrustedVideoPlugin::DisableImageExport, dd9811f7-7a9f-4b7e-8425-cb25efe0a71d, evr/IEVRTrustedVideoPlugin::DisableImageExport, mf.ievrtrustedvideoplugin_disableimageexport
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
 - IEVRTrustedVideoPlugin::DisableImageExport
 - evr/IEVRTrustedVideoPlugin::DisableImageExport
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
 - IEVRTrustedVideoPlugin.DisableImageExport
archived: true
---

# IEVRTrustedVideoPlugin::DisableImageExport


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Enables or disables the ability of the plug-in to export the video image.

## -parameters

### -param bDisable [in]

Boolean value. Specify <b>TRUE</b> to disable image exporting, or <b>FALSE</b> to enable it.

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

An EVR plug-in might expose a way for the application to get a copy of the video frames. For example, the standard EVR presenter implements <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getcurrentimage">IMFVideoDisplayControl::GetCurrentImage</a>.

If the plug-in supports image exporting, this method enables or disables it. Before this method has been called for the first time, the EVR assumes that the mechanism is enabled.

If the plug-in does not support image exporting, this method should return S_OK and ignore the value of <i>bDisable</i>. If the method fails, the EVR treats it as a failure to enforce the policy, which will probably cause playback to stop.

While image exporting is disabled, any associated export method, such as <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getcurrentimage">GetCurrentImage</a>, should return MF_E_LICENSE_INCORRECT_RIGHTS.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin">IEVRTrustedVideoPlugin</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>