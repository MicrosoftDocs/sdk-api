---
UID: NF:wiavideo.IWiaVideo.ResizeVideo
title: IWiaVideo::ResizeVideo
author: windows-driver-content
description: The IWiaVideo::ResizeVideo method resizes the video playback to the largest supported resolution that fits inside the parent window. Call this method whenever the parent window is moved or resized.
old-location: wia\_wia_IWiaVideo_ResizeVideo.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\resizevideo.htm
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IWiaVideo interface [WIA],ResizeVideo method, IWiaVideo.ResizeVideo, IWiaVideo::ResizeVideo, ResizeVideo, ResizeVideo method [WIA], ResizeVideo method [WIA],IWiaVideo interface, _wia_IWiaVideo_ResizeVideo, wia._wia_IWiaVideo_ResizeVideo, wiavideo/IWiaVideo::ResizeVideo
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiavideo.dll
api_name:
-	IWiaVideo.ResizeVideo
product: Windows
targetos: Windows
req.lib: 
req.dll: Wiavideo.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaVideo::ResizeVideo


## -description


The <b>IWiaVideo::ResizeVideo</b> method resizes the video playback to the largest supported resolution that fits inside the parent window. Call this method whenever the parent window is moved or resized.


## -parameters




### -param bStretchToFitParent [in]

Type: <b>BOOL</b>

Specifies whether the video playback is stretched to fill the parent window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



By default, the video is displayed in a supported resolution smaller than the parent window. If <i>bStretchToFitParent</i> is set to <b>TRUE</b>, the video display fills the window.



