---
UID: NF:wincodec.IWICDevelopRawNotificationCallback.Notify
title: IWICDevelopRawNotificationCallback::Notify (wincodec.h)
description: An application-defined callback method used for raw image parameter change notifications.
helpviewer_keywords: ["IWICDevelopRawNotificationCallback interface [Windows Imaging Component]","Notify method","IWICDevelopRawNotificationCallback.Notify","IWICDevelopRawNotificationCallback::Notify","Notify","Notify method [Windows Imaging Component]","Notify method [Windows Imaging Component]","IWICDevelopRawNotificationCallback interface","_wic_codec_iwicdeveloprawnotificationcallback_notify","wic._wic_codec_iwicdeveloprawnotificationcallback_notify","wincodec/IWICDevelopRawNotificationCallback::Notify"]
old-location: wic\_wic_codec_iwicdeveloprawnotificationcallback_notify.htm
tech.root: wic
ms.assetid: a91fb8e8-a4f4-4a6d-87d0-00bf2ef205e6
ms.date: 12/05/2018
ms.keywords: IWICDevelopRawNotificationCallback interface [Windows Imaging Component],Notify method, IWICDevelopRawNotificationCallback.Notify, IWICDevelopRawNotificationCallback::Notify, Notify, Notify method [Windows Imaging Component], Notify method [Windows Imaging Component],IWICDevelopRawNotificationCallback interface, _wic_codec_iwicdeveloprawnotificationcallback_notify, wic._wic_codec_iwicdeveloprawnotificationcallback_notify, wincodec/IWICDevelopRawNotificationCallback::Notify
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
 - IWICDevelopRawNotificationCallback::Notify
 - wincodec/IWICDevelopRawNotificationCallback::Notify
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
 - IWICDevelopRawNotificationCallback.Notify
---

# IWICDevelopRawNotificationCallback::Notify


## -description

An application-defined callback method used for raw image parameter change notifications.

## -parameters

### -param NotificationMask [in]

Type: <b>UINT</b>

A set of <a href="/windows/desktop/wic/-wic-codec-iwicdeveloprawnotification-constants">IWICDevelopRawNotificationCallback Constants</a> parameter notification flags.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.