---
UID: NF:mfmediaengine.IMFMediaEngineEx.EnableWindowlessSwapchainMode
title: IMFMediaEngineEx::EnableWindowlessSwapchainMode
author: windows-driver-content
description: Enables or disables windowless swap-chain mode.
old-location: mf\imfmediaengineex_enablewindowlessswapchainmode.htm
old-project: medfound
ms.assetid: B93429D7-A0DF-4440-A164-C140334FC0A6
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: EnableWindowlessSwapchainMode, EnableWindowlessSwapchainMode method [Media Foundation], EnableWindowlessSwapchainMode method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],EnableWindowlessSwapchainMode method, IMFMediaEngineEx.EnableWindowlessSwapchainMode, IMFMediaEngineEx::EnableWindowlessSwapchainMode, mf.imfmediaengineex_enablewindowlessswapchainmode, mfmediaengine/IMFMediaEngineEx::EnableWindowlessSwapchainMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineEx.EnableWindowlessSwapchainMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineEx::EnableWindowlessSwapchainMode


## -description


Enables or disables windowless swap-chain mode.


## -parameters




### -param fEnable [in]

If <b>TRUE</b>, windowless swap-chain mode is enabled. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In windowless swap-chain mode, the Media Engine creates a windowless swap chain and presents video frames to the swap chain. To render the video, call <a href="https://msdn.microsoft.com/23AE2296-F0BF-4060-9849-F6A0E0C13B86">IMFMediaEngineEx::GetVideoSwapchainHandle</a> to get a handle to the swap chain, and then associate the handle with a Microsoft DirectComposition visual.  




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

