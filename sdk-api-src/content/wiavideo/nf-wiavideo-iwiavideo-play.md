---
UID: NF:wiavideo.IWiaVideo.Play
title: IWiaVideo::Play (wiavideo.h)
author: windows-sdk-content
description: Begins playback of streaming video.
old-location: wia\_wia_IWiaVideo_Play.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\play.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaVideo interface [WIA],Play method, IWiaVideo.Play, IWiaVideo::Play, Play, Play method [WIA], Play method [WIA],IWiaVideo interface, _wia_IWiaVideo_Play, wia._wia_IWiaVideo_Play, wiavideo/IWiaVideo::Play
ms.topic: method
f1_keywords: 
 - "wiavideo/IWiaVideo.Play"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiavideo.dll
api_name:
 - IWiaVideo.Play
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWiaVideo::Play


## -description


Begins playback of streaming video.


## -parameters






## -returns



Type: <b>HRESULT</b>

If the method succeeds or the video is already playing, this method returns S_OK. If the method fails, it returns a standard COM error code.




## -remarks



Call this method only after a successful call to <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobydevnum">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobyname">IWiaVideo::CreateVideoByName</a>.



