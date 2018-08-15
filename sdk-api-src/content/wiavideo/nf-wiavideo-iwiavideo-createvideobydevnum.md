---
UID: NF:wiavideo.IWiaVideo.CreateVideoByDevNum
title: IWiaVideo::CreateVideoByDevNum
author: windows-sdk-content
description: The IWiaVideo::CreateVideoByDevNum method creates a connection to a streaming video device with the device number obtained from a Directshow enumeration.
old-location: wia\_wia_IWiaVideo_CreateVideoByDevNum.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\createvideobydevnum.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateVideoByDevNum, CreateVideoByDevNum method [WIA], CreateVideoByDevNum method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],CreateVideoByDevNum method, IWiaVideo.CreateVideoByDevNum, IWiaVideo::CreateVideoByDevNum, _wia_IWiaVideo_CreateVideoByDevNum, wia._wia_IWiaVideo_CreateVideoByDevNum, wiavideo/IWiaVideo::CreateVideoByDevNum
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
 - IWiaVideo.CreateVideoByDevNum
product: Windows
targetos: Windows
req.lib: 
req.dll: Wiavideo.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaVideo::CreateVideoByDevNum


## -description


The <b>IWiaVideo::CreateVideoByDevNum</b> method creates a connection to a streaming video device with the device number obtained from a Directshow enumeration.


## -parameters




### -param uiDeviceNumber [in]

Type: <b>UINT</b>

Specifies the video device's Directshow device number.


### -param hwndParent [in]

Type: <b>HWND</b>

Specifies the window in which to display the streaming video.


### -param bStretchToFitParent [in]

Type: <b>BOOL</b>

Specifies whether the video display is stretched to fit the parent window. Set this parameter to <b>TRUE</b> if the display should be stretched to fit the parent window; otherwise, set to <b>FALSE</b>.


### -param bAutoBeginPlayback [in]

Type: <b>BOOL</b>

Specifies whether the streaming video begins playback as soon as this method returns. Set this parameter to <b>TRUE</b> to cause immediate playback; set it to <b>FALSE</b> to require a call to <a href="https://msdn.microsoft.com/en-us/library/ms629900(v=VS.85).aspx">IWiaVideo::Play</a> before video playback begins.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



By default, the video is displayed in the video device's default resolution. If <i>bStretchToFitParent</i> is set to <b>TRUE</b>, the video display fills the window.



