---
UID: NF:wiavideo.IWiaVideo.DestroyVideo
title: IWiaVideo::DestroyVideo (wiavideo.h)
description: The IWiaVideo::DestroyVideo method shuts down the streaming video. To restart video playback, the application must call one of the IWiaVideo CreateVideo methods again.
helpviewer_keywords: ["DestroyVideo","DestroyVideo method [WIA]","DestroyVideo method [WIA]","IWiaVideo interface","IWiaVideo interface [WIA]","DestroyVideo method","IWiaVideo.DestroyVideo","IWiaVideo::DestroyVideo","_wia_IWiaVideo_DestroyVideo","wia._wia_IWiaVideo_DestroyVideo","wiavideo/IWiaVideo::DestroyVideo"]
old-location: wia\_wia_IWiaVideo_DestroyVideo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\destroyvideo.htm
ms.date: 12/05/2018
ms.keywords: DestroyVideo, DestroyVideo method [WIA], DestroyVideo method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],DestroyVideo method, IWiaVideo.DestroyVideo, IWiaVideo::DestroyVideo, _wia_IWiaVideo_DestroyVideo, wia._wia_IWiaVideo_DestroyVideo, wiavideo/IWiaVideo::DestroyVideo
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
 - IWiaVideo::DestroyVideo
 - wiavideo/IWiaVideo::DestroyVideo
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
 - IWiaVideo.DestroyVideo
archived: true
---

# IWiaVideo::DestroyVideo


## -description

The <b>IWiaVideo::DestroyVideo</b> method shuts down the streaming video. To restart video playback, the application must call one of the <a href="/windows/desktop/api/wiavideo/nn-wiavideo-iwiavideo">IWiaVideo</a> CreateVideo methods again.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method only after a successful call to <a href="/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobydevnum">IWiaVideo::CreateVideoByDevNum</a>, or <a href="/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobyname">IWiaVideo::CreateVideoByName</a>.
