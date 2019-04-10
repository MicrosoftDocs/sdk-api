---
UID: NC:wincodec.PFNProgressNotification
title: PFNProgressNotification (wincodec.h)
author: windows-sdk-content
description: Application defined callback function called when codec component progress is made.
old-location: wic\_wic_codec_progressnotificationcallback.htm
tech.root: wic
ms.assetid: 10dd9fbe-abff-4fc9-a3a5-7c01ecc10a7f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PFNProgressNotification, PFNProgressNotification callback, ProgressNotificationCallback, ProgressNotificationCallback callback function [Windows Imaging Component], _wic_codec_progressnotificationcallback, wic._wic_codec_progressnotificationcallback, wincodec/ProgressNotificationCallback
ms.topic: callback
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincodec.h
api_name:
 - ProgressNotificationCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNProgressNotification callback function


## -description


Application defined callback function called when codec component progress is made.


## -parameters




### -param pvData

Type: <b>LPVOID</b>

Component data passed to the callback function.


### -param uFrameNum

Type: <b>ULONG</b>

The current frame number.


### -param operation

Type: <b><a href="https://msdn.microsoft.com/407b982d-7232-42ce-9ff5-7029b7d922a4">WICProgressOperation</a></b>

The current operation the component is in.


### -param dblProgress

Type: <b>double</b>

The progress value. The range is 0.0 to 1.0.


## -returns



Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An operation can be canceled by returning <code>WINCODEC_ERR_ABORTED</code>.

To register your callback function, query the encoder or decoder for the <a href="https://msdn.microsoft.com/8cf3fbca-0953-4dd7-aa44-3e1924cfd8b0">IWICBitmapCodecProgressNotification</a> interface and call <a href="https://msdn.microsoft.com/ac47178a-f149-4313-8673-ece59e88cfb3">RegisterProgressNotification</a>.




## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/6d7ef6f1-2024-4de5-9c2e-8edc6359f79b">WICProgressNotification</a>



<a href="https://msdn.microsoft.com/407b982d-7232-42ce-9ff5-7029b7d922a4">WICProgressOperation</a>
 

 

