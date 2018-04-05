---
UID: NF:wincodec.IWICDevelopRawNotificationCallback.Notify
title: IWICDevelopRawNotificationCallback::Notify method
author: windows-driver-content
description: An application-defined callback method used for raw image parameter change notifications.
old-location: wic\_wic_codec_iwicdeveloprawnotificationcallback_notify.htm
old-project: wic
ms.assetid: a91fb8e8-a4f4-4a6d-87d0-00bf2ef205e6
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IWICDevelopRawNotificationCallback, IWICDevelopRawNotificationCallback interface [Windows Imaging Component], Notify method, IWICDevelopRawNotificationCallback::Notify, Notify method [Windows Imaging Component], Notify method [Windows Imaging Component], IWICDevelopRawNotificationCallback interface, Notify,IWICDevelopRawNotificationCallback.Notify, _wic_codec_iwicdeveloprawnotificationcallback_notify, wic._wic_codec_iwicdeveloprawnotificationcallback_notify, wincodec/IWICDevelopRawNotificationCallback::Notify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.lib
-	Windowscodecs.dll
api_name:
-	IWICDevelopRawNotificationCallback.Notify
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRawNotificationCallback::Notify method


## -description


An application-defined callback method used for raw image parameter change notifications.


## -parameters




### -param NotificationMask [in]

Type: <b>UINT</b>

A set of <a href="https://msdn.microsoft.com/4e94b4f4-abd9-4395-87ec-a08e49a2cf88">IWICDevelopRawNotificationCallback Constants</a> parameter notification flags.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



