---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_wiavideo_xp_0000_0000_0001 enumeration


## -description


The <b>WIAVIDEO_STATE</b> enumeration is used to specify the current state of a video stream.


<div class="alert"><b>Note</b>  Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use <a href="http://msdn.microsoft.com/en-us/library/ms783323(VS.85).aspx">DirectShow</a> to acquire images from video.</div><div> </div>

## -enum-fields




### -field WIAVIDEO_NO_VIDEO

No video stream exists. Call <a href="https://msdn.microsoft.com/bc5379fb-54ba-4bcd-b302-e07676885106">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://msdn.microsoft.com/0ea7ab75-7893-485d-a523-faa6019e1f67">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://msdn.microsoft.com/4ea34408-cf71-45d2-ac3b-6e3ad9622ae5">IWiaVideo::CreateVideoByName</a> to create a video.


### -field WIAVIDEO_CREATING_VIDEO

One of the <a href="https://msdn.microsoft.com/aed8bc1d-7b59-4276-a63f-8d9401faab1a">IWiaVideo</a> CreateVideo methods was called and WIA is in the process of creating the video stream.


### -field WIAVIDEO_VIDEO_CREATED

A video stream has been successfully created, but playback has not yet started.


### -field WIAVIDEO_VIDEO_PLAYING

A video stream has been successfully created, and the video is playing. The application can now call the <a href="https://msdn.microsoft.com/edd4b242-f4df-4f5b-8655-e697e78fef47">IWiaVideo::TakePicture</a> method.


### -field WIAVIDEO_VIDEO_PAUSED

A video stream has been successfully created, and the video is paused. The application can now call the <a href="https://msdn.microsoft.com/edd4b242-f4df-4f5b-8655-e697e78fef47">IWiaVideo::TakePicture</a> method.


### -field WIAVIDEO_DESTROYING_VIDEO

The application called <a href="https://msdn.microsoft.com/9c175fb1-8d3f-47a5-98d6-8f7d256b8f4e">IWiaVideo::DestroyVideo</a> method, and WIA is in the process of destroying the video stream.


## -see-also




<a href="https://msdn.microsoft.com/ccd5abb6-8baa-4751-a8f8-5120c78739b4">IWiaVideo::GetCurrentState</a>
 

 

