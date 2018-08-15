---
UID: NF:wiavideo.IWiaVideo.GetCurrentState
title: IWiaVideo::GetCurrentState
author: windows-sdk-content
description: The IWiaVideo::GetCurrentState method specifies the state of the video stream as a member of the WIAVIDEO_STATE enumeration.
old-location: wia\_wia_IWiaVideo_GetCurrentState.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\getcurrentstate.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCurrentState, GetCurrentState method [WIA], GetCurrentState method [WIA],IWiaVideo interface, IWiaVideo interface [WIA],GetCurrentState method, IWiaVideo.GetCurrentState, IWiaVideo::GetCurrentState, _wia_IWiaVideo_GetCurrentState, wia._wia_IWiaVideo_GetCurrentState, wiavideo/IWiaVideo::GetCurrentState
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
 - IWiaVideo.GetCurrentState
product: Windows
targetos: Windows
req.lib: 
req.dll: Wiavideo.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaVideo::GetCurrentState


## -description


The <b>IWiaVideo::GetCurrentState</b> method specifies the state of the video stream as a member of the <a href="https://msdn.microsoft.com/3d460ca8-6760-4649-b33d-ebf24d318346">WIAVIDEO_STATE</a> enumeration.


## -parameters




### -param pState [out, retval]

Type: <b><a href="https://msdn.microsoft.com/3d460ca8-6760-4649-b33d-ebf24d318346">WIAVIDEO_STATE</a>*</b>

A member of the <a href="https://msdn.microsoft.com/3d460ca8-6760-4649-b33d-ebf24d318346">WIAVIDEO_STATE</a> enumeration that specifies the current state of the video stream.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



