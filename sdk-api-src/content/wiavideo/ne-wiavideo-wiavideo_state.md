---
UID: NE:wiavideo.__MIDL___MIDL_itf_wiavideo_xp_0000_0000_0001
title: WIAVIDEO_STATE (wiavideo.h)
description: The WIAVIDEO_STATE enumeration is used to specify the current state of a video stream.helpviewer_keywords: ["WIAVIDEO_CREATING_VIDEO","WIAVIDEO_DESTROYING_VIDEO","WIAVIDEO_NO_VIDEO","WIAVIDEO_STATE","WIAVIDEO_STATE enumeration [WIA]","WIAVIDEO_VIDEO_CREATED","WIAVIDEO_VIDEO_PAUSED","WIAVIDEO_VIDEO_PLAYING","_wia_WIAVIDEO_STATE","wia._wia_WIAVIDEO_STATE","wiavideo/WIAVIDEO_CREATING_VIDEO","wiavideo/WIAVIDEO_DESTROYING_VIDEO","wiavideo/WIAVIDEO_NO_VIDEO","wiavideo/WIAVIDEO_STATE","wiavideo/WIAVIDEO_VIDEO_CREATED","wiavideo/WIAVIDEO_VIDEO_PAUSED","wiavideo/WIAVIDEO_VIDEO_PLAYING"]
old-location: wia\_wia_WIAVIDEO_STATE.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\enums\wiavideo_state.htm
ms.date: 12/05/2018
ms.keywords: WIAVIDEO_CREATING_VIDEO, WIAVIDEO_DESTROYING_VIDEO, WIAVIDEO_NO_VIDEO, WIAVIDEO_STATE, WIAVIDEO_STATE enumeration [WIA], WIAVIDEO_VIDEO_CREATED, WIAVIDEO_VIDEO_PAUSED, WIAVIDEO_VIDEO_PLAYING, _wia_WIAVIDEO_STATE, wia._wia_WIAVIDEO_STATE, wiavideo/WIAVIDEO_CREATING_VIDEO, wiavideo/WIAVIDEO_DESTROYING_VIDEO, wiavideo/WIAVIDEO_NO_VIDEO, wiavideo/WIAVIDEO_STATE, wiavideo/WIAVIDEO_VIDEO_CREATED, wiavideo/WIAVIDEO_VIDEO_PAUSED, wiavideo/WIAVIDEO_VIDEO_PLAYING
f1_keywords:
- wiavideo/WIAVIDEO_STATE
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wiavideo.h
api_name:
- WIAVIDEO_STATE
targetos: Windows
req.typenames: WIAVIDEO_STATE
req.redist: 
ms.custom: 19H1
---

# WIAVIDEO_STATE enumeration


## -description


The <b>WIAVIDEO_STATE</b> enumeration is used to specify the current state of a video stream.


<div class="alert"><b>Note</b>  Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use <a href="https://docs.microsoft.com/previous-versions/ms783323(v=vs.85)">DirectShow</a> to acquire images from video.</div><div> </div>

## -enum-fields




### -field WIAVIDEO_NO_VIDEO

No video stream exists. Call <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobydevnum">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobyname">IWiaVideo::CreateVideoByName</a> to create a video.


### -field WIAVIDEO_CREATING_VIDEO

One of the <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nn-wiavideo-iwiavideo">IWiaVideo</a> CreateVideo methods was called and WIA is in the process of creating the video stream.


### -field WIAVIDEO_VIDEO_CREATED

A video stream has been successfully created, but playback has not yet started.


### -field WIAVIDEO_VIDEO_PLAYING

A video stream has been successfully created, and the video is playing. The application can now call the <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-takepicture">IWiaVideo::TakePicture</a> method.


### -field WIAVIDEO_VIDEO_PAUSED

A video stream has been successfully created, and the video is paused. The application can now call the <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-takepicture">IWiaVideo::TakePicture</a> method.


### -field WIAVIDEO_DESTROYING_VIDEO

The application called <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-destroyvideo">IWiaVideo::DestroyVideo</a> method, and WIA is in the process of destroying the video stream.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-getcurrentstate">IWiaVideo::GetCurrentState</a>
 

 

