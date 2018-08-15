---
UID: NF:wiavideo.IWiaVideo.DestroyVideo
title: IWiaVideo::DestroyVideo
author: windows-sdk-content
description: The IWiaVideo::DestroyVideo method shuts down the streaming video. To restart video playback, the application must call one of the IWiaVideo CreateVideo methods again.
old-location: wia\_wia_IWiaVideo_DestroyVideo.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\destroyvideo.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DestroyVideo, DestroyVideo method [WIA], DestroyVideo method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],DestroyVideo method, IWiaVideo.DestroyVideo, IWiaVideo::DestroyVideo, _wia_IWiaVideo_DestroyVideo, wia._wia_IWiaVideo_DestroyVideo, wiavideo/IWiaVideo::DestroyVideo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wiavideo.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiavideo.dll
api_name:
 - IWiaVideo.DestroyVideo
product: Windows
targetos: Windows
req.lib: 
req.dll: Wiavideo.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaVideo::DestroyVideo


## -description


The <b>IWiaVideo::DestroyVideo</b> method shuts down the streaming video. To restart video playback, the application must call one of the <a href="https://msdn.microsoft.com/aed8bc1d-7b59-4276-a63f-8d9401faab1a">IWiaVideo</a> CreateVideo methods again.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method only after a successful call to <a href="https://msdn.microsoft.com/bc5379fb-54ba-4bcd-b302-e07676885106">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://msdn.microsoft.com/0ea7ab75-7893-485d-a523-faa6019e1f67">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://msdn.microsoft.com/4ea34408-cf71-45d2-ac3b-6e3ad9622ae5">IWiaVideo::CreateVideoByName</a>.



