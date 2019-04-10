---
UID: NF:wiavideo.IWiaVideo.DestroyVideo
title: IWiaVideo::DestroyVideo (wiavideo.h)
author: windows-sdk-content
description: The IWiaVideo::DestroyVideo method shuts down the streaming video. To restart video playback, the application must call one of the IWiaVideo CreateVideo methods again.
old-location: wia\_wia_IWiaVideo_DestroyVideo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\destroyvideo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DestroyVideo, DestroyVideo method [WIA], DestroyVideo method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],DestroyVideo method, IWiaVideo.DestroyVideo, IWiaVideo::DestroyVideo, _wia_IWiaVideo_DestroyVideo, wia._wia_IWiaVideo_DestroyVideo, wiavideo/IWiaVideo::DestroyVideo
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
 - IWiaVideo.DestroyVideo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaVideo::DestroyVideo


## -description


The <b>IWiaVideo::DestroyVideo</b> method shuts down the streaming video. To restart video playback, the application must call one of the <a href="https://msdn.microsoft.com/en-us/library/ms629896(v=VS.85).aspx">IWiaVideo</a> CreateVideo methods again.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method only after a successful call to <a href="https://msdn.microsoft.com/en-us/library/ms629889(v=VS.85).aspx">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://msdn.microsoft.com/en-us/library/ms629884(v=VS.85).aspx">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms629886(v=VS.85).aspx">IWiaVideo::CreateVideoByName</a>.



