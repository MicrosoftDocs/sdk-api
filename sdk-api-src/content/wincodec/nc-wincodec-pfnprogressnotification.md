---
UID: NC:wincodec.PFNProgressNotification
title: PFNProgressNotification (wincodec.h)
description: Application defined callback function called when codec component progress is made.
helpviewer_keywords: ["PFNProgressNotification","PFNProgressNotification callback","ProgressNotificationCallback","ProgressNotificationCallback callback function [Windows Imaging Component]","_wic_codec_progressnotificationcallback","wic._wic_codec_progressnotificationcallback","wincodec/ProgressNotificationCallback"]
old-location: wic\_wic_codec_progressnotificationcallback.htm
tech.root: wic
ms.assetid: 10dd9fbe-abff-4fc9-a3a5-7c01ecc10a7f
ms.date: 12/05/2018
ms.keywords: PFNProgressNotification, PFNProgressNotification callback, ProgressNotificationCallback, ProgressNotificationCallback callback function [Windows Imaging Component], _wic_codec_progressnotificationcallback, wic._wic_codec_progressnotificationcallback, wincodec/ProgressNotificationCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNProgressNotification
 - wincodec/PFNProgressNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincodec.h
api_name:
 - ProgressNotificationCallback
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

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicprogressoperation">WICProgressOperation</a></b>

The current operation the component is in.

### -param dblProgress

Type: <b>double</b>

The progress value. The range is 0.0 to 1.0.

## -returns

Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An operation can be canceled by returning <code>WINCODEC_ERR_ABORTED</code>.

To register your callback function, query the encoder or decoder for the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapcodecprogressnotification">IWICBitmapCodecProgressNotification</a> interface and call <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification">RegisterProgressNotification</a>.

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/wincodec/ne-wincodec-wicprogressnotification">WICProgressNotification</a>



<a href="/windows/desktop/api/wincodec/ne-wincodec-wicprogressoperation">WICProgressOperation</a>