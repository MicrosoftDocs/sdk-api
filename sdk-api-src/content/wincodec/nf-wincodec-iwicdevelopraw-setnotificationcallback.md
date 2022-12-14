---
UID: NF:wincodec.IWICDevelopRaw.SetNotificationCallback
title: IWICDevelopRaw::SetNotificationCallback (wincodec.h)
description: Sets the notification callback method.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetNotificationCallback method","IWICDevelopRaw.SetNotificationCallback","IWICDevelopRaw::SetNotificationCallback","SetNotificationCallback","SetNotificationCallback method [Windows Imaging Component]","SetNotificationCallback method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_setnotificationcallback","wic._wic_codec_iwicdevelopraw_setnotificationcallback","wincodec/IWICDevelopRaw::SetNotificationCallback"]
old-location: wic\_wic_codec_iwicdevelopraw_setnotificationcallback.htm
tech.root: wic
ms.assetid: f6c44dee-8dbd-49c2-9773-899b3f01b968
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetNotificationCallback method, IWICDevelopRaw.SetNotificationCallback, IWICDevelopRaw::SetNotificationCallback, SetNotificationCallback, SetNotificationCallback method [Windows Imaging Component], SetNotificationCallback method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setnotificationcallback, wic._wic_codec_iwicdevelopraw_setnotificationcallback, wincodec/IWICDevelopRaw::SetNotificationCallback
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
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICDevelopRaw::SetNotificationCallback
 - wincodec/IWICDevelopRaw::SetNotificationCallback
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
 - IWICDevelopRaw.SetNotificationCallback
---

# IWICDevelopRaw::SetNotificationCallback


## -description

Sets the notification callback method.

## -parameters

### -param pCallback [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicdeveloprawnotificationcallback">IWICDevelopRawNotificationCallback</a>*</b>

Pointer to the notification callback method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.