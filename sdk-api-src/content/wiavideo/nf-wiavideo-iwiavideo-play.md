---
UID: NF:wiavideo.IWiaVideo.Play
title: IWiaVideo::Play
author: windows-sdk-content
description: Begins playback of streaming video.
old-location: wia\_wia_IWiaVideo_Play.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\play.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWiaVideo interface [WIA],Play method, IWiaVideo.Play, IWiaVideo::Play, Play, Play method [WIA], Play method [WIA],IWiaVideo interface, _wia_IWiaVideo_Play, wia._wia_IWiaVideo_Play, wiavideo/IWiaVideo::Play
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaVideo::Play


## -description


Begins playback of streaming video.


## -parameters






## -returns



Type: <b>HRESULT</b>

If the method succeeds or the video is already playing, this method returns S_OK. If the method fails, it returns a standard COM error code.




## -remarks



Call this method only after a successful call to <a href="https://msdn.microsoft.com/bc5379fb-54ba-4bcd-b302-e07676885106">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://msdn.microsoft.com/0ea7ab75-7893-485d-a523-faa6019e1f67">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://msdn.microsoft.com/4ea34408-cf71-45d2-ac3b-6e3ad9622ae5">IWiaVideo::CreateVideoByName</a>.



