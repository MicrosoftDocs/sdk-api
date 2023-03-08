---
UID: NF:wincodec.IWICProgressCallback.Notify
title: IWICProgressCallback::Notify (wincodec.h)
description: Notify method is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use RegisterProgressNotification.
helpviewer_keywords: ["IWICProgressCallback interface [Windows Imaging Component]","Notify method","IWICProgressCallback.Notify","IWICProgressCallback::Notify","Notify","Notify method [Windows Imaging Component]","Notify method [Windows Imaging Component]","IWICProgressCallback interface","_wic_codec_iwicprogresscallback_notify","wic._wic_codec_iwicprogresscallback_notify","wincodec/IWICProgressCallback::Notify"]
old-location: wic\_wic_codec_iwicprogresscallback_notify.htm
tech.root: wic
ms.assetid: afbbfa87-716c-4957-9f90-d48d02d642e0
ms.date: 12/05/2018
ms.keywords: IWICProgressCallback interface [Windows Imaging Component],Notify method, IWICProgressCallback.Notify, IWICProgressCallback::Notify, Notify, Notify method [Windows Imaging Component], Notify method [Windows Imaging Component],IWICProgressCallback interface, _wic_codec_iwicprogresscallback_notify, wic._wic_codec_iwicprogresscallback_notify, wincodec/IWICProgressCallback::Notify
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICProgressCallback::Notify
 - wincodec/IWICProgressCallback::Notify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICProgressCallback.Notify
---

# IWICProgressCallback::Notify


## -description

<b>Notify</b> method is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification">RegisterProgressNotification</a>.

## -parameters

### -param uFrameNum [in]

Type: <b>ULONG</b>

The current frame number.

### -param operation [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicprogressoperation">WICProgressOperation</a></b>

The operation on which progress is being reported.

### -param dblProgress [in]

Type: <b>double</b>

The progress value ranging from is 0.0 to 1.0. 0.0 indicates the beginning of the operation. 1.0 indicates the end of the operation.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicprogresscallback">IWICProgressCallback</a>