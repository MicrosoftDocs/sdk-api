---
UID: NF:wiavideo.IWiaVideo.CreateVideoByWiaDevID
title: IWiaVideo::CreateVideoByWiaDevID (wiavideo.h)
description: The IWiaVideo::CreateVideoByWiaDevID method creates a connection to a streaming video device from its WIA_DIP_DEV_ID property.
helpviewer_keywords: ["CreateVideoByWiaDevID","CreateVideoByWiaDevID method [WIA]","CreateVideoByWiaDevID method [WIA]","IWiaVideo interface","IWiaVideo interface [WIA]","CreateVideoByWiaDevID method","IWiaVideo.CreateVideoByWiaDevID","IWiaVideo::CreateVideoByWiaDevID","_wia_IWiaVideo_CreateVideoByWiaDevID","wia._wia_IWiaVideo_CreateVideoByWiaDevID","wiavideo/IWiaVideo::CreateVideoByWiaDevID"]
old-location: wia\_wia_IWiaVideo_CreateVideoByWiaDevID.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\createvideobywiadevid.htm
ms.date: 12/05/2018
ms.keywords: CreateVideoByWiaDevID, CreateVideoByWiaDevID method [WIA], CreateVideoByWiaDevID method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],CreateVideoByWiaDevID method, IWiaVideo.CreateVideoByWiaDevID, IWiaVideo::CreateVideoByWiaDevID, _wia_IWiaVideo_CreateVideoByWiaDevID, wia._wia_IWiaVideo_CreateVideoByWiaDevID, wiavideo/IWiaVideo::CreateVideoByWiaDevID
req.header: wiavideo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Wiavideo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaVideo::CreateVideoByWiaDevID
 - wiavideo/IWiaVideo::CreateVideoByWiaDevID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiavideo.dll
api_name:
 - IWiaVideo.CreateVideoByWiaDevID
archived: true
---

# IWiaVideo::CreateVideoByWiaDevID


## -description

The <b>IWiaVideo::CreateVideoByWiaDevID</b> method creates a connection to a streaming video device from its WIA_DIP_DEV_ID property.

## -parameters

### -param bstrWiaDeviceID [in]

Type: <b>BSTR</b>

Specifies the value of the video device's WIA_DIP_DEV_ID property.

### -param hwndParent [in]

Type: <b>HWND</b>

Specifies the window in which to display the streaming video.

### -param bStretchToFitParent [in]

Type: <b>BOOL</b>

Specifies whether the video display is stretched to fit the parent window. Set this parameter to <b>TRUE</b> if the display should be stretched to fit the parent window; otherwise, set to <b>FALSE</b>.

### -param bAutoBeginPlayback [in]

Type: <b>BOOL</b>

Specifies whether the streaming video begins playback as soon as this method returns. Set this parameter to <b>TRUE</b> to cause immediate playback; set it to <b>FALSE</b> to require a call to <a href="/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-play">IWiaVideo::Play</a> before video playback begins.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

By default, the video is displayed in the video device's default resolution. If <i>bStretchToFitParent</i> is set to <b>TRUE</b>, the video display fills the window.

In order for the function to succeed, the <a href="/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory">IWiaVideo::ImagesDirectory</a> property must be specified first.  Thus, the caller must first call "put_ImagesDirectory" to specify the full path of the directory in which the captured still images will be stored.

## -see-also

<a href="/windows/desktop/wia/-wia-enumerating-system-devices">Enumerating System Devices</a>



<a href="/windows/desktop/api/wiavideo/nn-wiavideo-iwiavideo">IWiaVideo</a>