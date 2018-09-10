---
UID: NF:wiavideo.IWiaVideo.CreateVideoByWiaDevID
title: IWiaVideo::CreateVideoByWiaDevID
author: windows-sdk-content
description: The IWiaVideo::CreateVideoByWiaDevID method creates a connection to a streaming video device from its WIA_DIP_DEV_ID property.
old-location: wia\_wia_IWiaVideo_CreateVideoByWiaDevID.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\createvideobywiadevid.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateVideoByWiaDevID, CreateVideoByWiaDevID method [WIA], CreateVideoByWiaDevID method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],CreateVideoByWiaDevID method, IWiaVideo.CreateVideoByWiaDevID, IWiaVideo::CreateVideoByWiaDevID, _wia_IWiaVideo_CreateVideoByWiaDevID, wia._wia_IWiaVideo_CreateVideoByWiaDevID, wiavideo/IWiaVideo::CreateVideoByWiaDevID
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
 - IWiaVideo.CreateVideoByWiaDevID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaVideo::CreateVideoByWiaDevID


## -description


The <b>IWiaVideo::CreateVideoByWiaDevID</b> method creates a connection to a streaming video device from its WIA_DIP_DEV_ID property.


## -parameters




### -param bstrWiaDeviceID [in]

Type: <b>BSTR</b>

Specifies the value of the video device's WIA_DIP_DEV_ID property.


### -param hwndParent [in]

Type: <b>HWND</b>

Specifies the window in which to display the streaming video.


### -param bStretchToFitParent [in]

Type: <b>BOOL</b>

Specifies whether the video display is stretched to fit the parent window. Set this parameter to <b>TRUE</b> if the display should be stretched to fit the parent window; otherwise, set to <b>FALSE</b>.


### -param bAutoBeginPlayback [in]

Type: <b>BOOL</b>

Specifies whether the streaming video begins playback as soon as this method returns. Set this parameter to <b>TRUE</b> to cause immediate playback; set it to <b>FALSE</b> to require a call to <a href="https://msdn.microsoft.com/b8917c5f-6569-496d-a2ed-bd5ed76dfbcf">IWiaVideo::Play</a> before video playback begins.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



By default, the video is displayed in the video device's default resolution. If <i>bStretchToFitParent</i> is set to <b>TRUE</b>, the video display fills the window.

In order for the function to succeed, the <a href="https://msdn.microsoft.com/f7bff8d2-1cdd-4d32-877b-c61343888a26">IWiaVideo::ImagesDirectory</a> property must be specified first.  Thus, the caller must first call "put_ImagesDirectory" to specify the full path of the directory in which the captured still images will be stored.




## -see-also




<a href="https://msdn.microsoft.com/6465a33e-1b3b-4142-a58f-b27e9c95cd3e">Enumerating System Devices</a>



<a href="https://msdn.microsoft.com/aed8bc1d-7b59-4276-a63f-8d9401faab1a">IWiaVideo</a>
 

 

