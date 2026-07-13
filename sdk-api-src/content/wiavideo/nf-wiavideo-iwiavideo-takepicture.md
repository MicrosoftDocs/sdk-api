---
UID: NF:wiavideo.IWiaVideo.TakePicture
title: IWiaVideo::TakePicture (wiavideo.h)
description: The IWiaVideo::TakePicture method extracts a still image from the video stream, and saves the image as a JPEG file.
helpviewer_keywords: ["IWiaVideo interface [WIA]","TakePicture method","IWiaVideo.TakePicture","IWiaVideo::TakePicture","TakePicture","TakePicture method [WIA]","TakePicture method [WIA]","IWiaVideo interface","_wia_IWiaVideo_TakePicture","wia._wia_IWiaVideo_TakePicture","wiavideo/IWiaVideo::TakePicture"]
old-location: wia\_wia_IWiaVideo_TakePicture.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\takepicture.htm
ms.date: 12/05/2018
ms.keywords: IWiaVideo interface [WIA],TakePicture method, IWiaVideo.TakePicture, IWiaVideo::TakePicture, TakePicture, TakePicture method [WIA], TakePicture method [WIA],IWiaVideo interface, _wia_IWiaVideo_TakePicture, wia._wia_IWiaVideo_TakePicture, wiavideo/IWiaVideo::TakePicture
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaVideo::TakePicture
 - wiavideo/IWiaVideo::TakePicture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiavideo.dll
api_name:
 - IWiaVideo.TakePicture
archived: true
---

# IWiaVideo::TakePicture


## -description

The <b>IWiaVideo::TakePicture</b> method extracts a still image from the video stream, and saves the image as a JPEG file.

## -parameters

### -param pbstrNewImageFilename [out]

Type: <b>BSTR*</b>

Receives the full path and filename of the JPEG file that this method creates.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The path and directory where the image file is saved are specified by the <a href="/windows/desktop/api/wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory">IWiaVideo::ImagesDirectory</a> property.