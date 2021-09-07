---
UID: NF:wincodec.IWICBitmapCodecProgressNotification.RegisterProgressNotification
title: IWICBitmapCodecProgressNotification::RegisterProgressNotification (wincodec.h)
description: Registers a progress notification callback function.
helpviewer_keywords: ["IWICBitmapCodecProgressNotification interface [Windows Imaging Component]","RegisterProgressNotification method","IWICBitmapCodecProgressNotification.RegisterProgressNotification","IWICBitmapCodecProgressNotification::RegisterProgressNotification","RegisterProgressNotification","RegisterProgressNotification method [Windows Imaging Component]","RegisterProgressNotification method [Windows Imaging Component]","IWICBitmapCodecProgressNotification interface","_wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification","wic._wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification","wincodec/IWICBitmapCodecProgressNotification::RegisterProgressNotification"]
old-location: wic\_wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification.htm
tech.root: wic
ms.assetid: ac47178a-f149-4313-8673-ece59e88cfb3
ms.date: 12/05/2018
ms.keywords: IWICBitmapCodecProgressNotification interface [Windows Imaging Component],RegisterProgressNotification method, IWICBitmapCodecProgressNotification.RegisterProgressNotification, IWICBitmapCodecProgressNotification::RegisterProgressNotification, RegisterProgressNotification, RegisterProgressNotification method [Windows Imaging Component], RegisterProgressNotification method [Windows Imaging Component],IWICBitmapCodecProgressNotification interface, _wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification, wic._wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification, wincodec/IWICBitmapCodecProgressNotification::RegisterProgressNotification
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapCodecProgressNotification::RegisterProgressNotification
 - wincodec/IWICBitmapCodecProgressNotification::RegisterProgressNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICBitmapCodecProgressNotification.RegisterProgressNotification
---

# IWICBitmapCodecProgressNotification::RegisterProgressNotification


## -description

Registers a progress notification callback function.

## -parameters

### -param pfnProgressNotification [in]

Type: <b>PFNProgressNotification</b>

A function pointer to the application defined progress notification callback function. See <a href="/windows/desktop/api/wincodec/nc-wincodec-pfnprogressnotification">ProgressNotificationCallback</a> for the callback signature.

### -param pvData [in]

Type: <b>LPVOID</b>

A pointer to component data for the callback method.

### -param dwProgressFlags [in]

Type: <b>DWORD</b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicprogressoperation">WICProgressOperation</a> and <a href="/windows/desktop/api/wincodec/ne-wincodec-wicprogressnotification">WICProgressNotification</a> flags to use for progress notification.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications can only register a single callback. Subsequent registration calls will replace the previously registered callback. To unregister a callback, pass in <b>NULL</b> or register a new callback function.

Progress is reported in an increasing order between 0.0 and 1.0. 
            If <i>dwProgressFlags</i> includes <b>WICProgressNotificationBegin</b>, the callback is guaranteed to be called with progress 0.0.
            If <i>dwProgressFlags</i> includes <b>WICProgressNotificationEnd</b>, the callback is guaranteed to be called with progress 1.0.
         

<b>WICProgressNotificationFrequent</b> increases the frequency in which the callback is called.
            If an operation is expected to take more than 30 seconds, <b>WICProgressNotificationFrequent</b> should be added to <i>dwProgressFlags</i>.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapcodecprogressnotification">IWICBitmapCodecProgressNotification</a>



<a href="/windows/desktop/api/wincodec/nc-wincodec-pfnprogressnotification">ProgressNotificationCallback</a>