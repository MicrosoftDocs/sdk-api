---
UID: NF:wiavideo.IWiaVideo.CreateVideoByDevNum
title: IWiaVideo::CreateVideoByDevNum (wiavideo.h)
description: The IWiaVideo::CreateVideoByDevNum method creates a connection to a streaming video device with the device number obtained from a Directshow enumeration.
helpviewer_keywords: ["CreateVideoByDevNum","CreateVideoByDevNum method [WIA]","CreateVideoByDevNum method [WIA]","IWiaVideo interface","IWiaVideo interface [WIA]","CreateVideoByDevNum method","IWiaVideo.CreateVideoByDevNum","IWiaVideo::CreateVideoByDevNum","_wia_IWiaVideo_CreateVideoByDevNum","wia._wia_IWiaVideo_CreateVideoByDevNum","wiavideo/IWiaVideo::CreateVideoByDevNum"]
old-location: wia\_wia_IWiaVideo_CreateVideoByDevNum.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\createvideobydevnum.htm
ms.date: 12/05/2018
ms.keywords: CreateVideoByDevNum, CreateVideoByDevNum method [WIA], CreateVideoByDevNum method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],CreateVideoByDevNum method, IWiaVideo.CreateVideoByDevNum, IWiaVideo::CreateVideoByDevNum, _wia_IWiaVideo_CreateVideoByDevNum, wia._wia_IWiaVideo_CreateVideoByDevNum, wiavideo/IWiaVideo::CreateVideoByDevNum
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
 - IWiaVideo::CreateVideoByDevNum
 - wiavideo/IWiaVideo::CreateVideoByDevNum
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
 - IWiaVideo.CreateVideoByDevNum
archived: true
---

# IWiaVideo::CreateVideoByDevNum


## -description

The <b>IWiaVideo::CreateVideoByDevNum</b> method creates a connection to a streaming video device with the device number obtained from a Directshow enumeration.

## -parameters

### -param uiDeviceNumber [in]

Type: <b>UINT</b>

Specifies the video device's Directshow device number.

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