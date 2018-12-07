---
UID: NF:wiavideo.IWiaVideo.Pause
title: IWiaVideo::Pause
author: windows-sdk-content
description: The IWiaVideo::Pause method pauses video playback.
old-location: wia\_wia_IWiaVideo_Pause.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\pause.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWiaVideo interface [WIA],Pause method, IWiaVideo.Pause, IWiaVideo::Pause, Pause, Pause method [WIA], Pause method [WIA],IWiaVideo interface, _wia_IWiaVideo_Pause, wia._wia_IWiaVideo_Pause, wiavideo/IWiaVideo::Pause
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
 - IWiaVideo.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaVideo::Pause


## -description


The <b>IWiaVideo::Pause</b> method pauses video playback.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method only after a successful call to <a href="https://msdn.microsoft.com/en-us/library/ms629889(v=VS.85).aspx">IWiaVideo::CreateVideoByWiaDevID</a>, <a href="https://msdn.microsoft.com/en-us/library/ms629884(v=VS.85).aspx">IWiaVideo::CreateVideoByDevNum</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms629886(v=VS.85).aspx">IWiaVideo::CreateVideoByName</a>.



