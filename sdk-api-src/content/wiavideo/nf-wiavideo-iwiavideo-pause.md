---
UID: NF:wiavideo.IWiaVideo.Pause
title: IWiaVideo::Pause (wiavideo.h)
author: windows-sdk-content
description: The IWiaVideo::Pause method pauses video playback.
old-location: wia\_wia_IWiaVideo_Pause.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\pause.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaVideo interface [WIA],Pause method, IWiaVideo.Pause, IWiaVideo::Pause, Pause, Pause method [WIA], Pause method [WIA],IWiaVideo interface, _wia_IWiaVideo_Pause, wia._wia_IWiaVideo_Pause, wiavideo/IWiaVideo::Pause
ms.topic: method
f1_keywords: ["wiavideo/IWiaVideo.Pause"]
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
 - IWiaVideo.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWiaVideo::Pause


## -description


The <b>IWiaVideo::Pause</b> method pauses video playback.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method only after a successful call to <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobydevnum">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-createvideobyname">IWiaVideo::CreateVideoByName</a>.



