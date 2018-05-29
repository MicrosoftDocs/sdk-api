---
UID: NF:wincodec.IWICDevelopRaw.SetNotificationCallback
title: IWICDevelopRaw::SetNotificationCallback
author: windows-sdk-content
description: Sets the notification callback method.
old-location: wic\_wic_codec_iwicdevelopraw_setnotificationcallback.htm
old-project: wic
ms.assetid: f6c44dee-8dbd-49c2-9773-899b3f01b968
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetNotificationCallback method, IWICDevelopRaw.SetNotificationCallback, IWICDevelopRaw::SetNotificationCallback, SetNotificationCallback, SetNotificationCallback method [Windows Imaging Component], SetNotificationCallback method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setnotificationcallback, wic._wic_codec_iwicdevelopraw_setnotificationcallback, wincodec/IWICDevelopRaw::SetNotificationCallback
ms.prod: windows
ms.technology: windows-sdk
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
-	Windowscodecs.dll
api_name:
-	IWICDevelopRaw.SetNotificationCallback
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::SetNotificationCallback


## -description


Sets the notification callback method.


## -parameters




### -param pCallback [in]

Type: <b><a href="https://msdn.microsoft.com/ccd162e4-84be-4ed5-a583-c9bd195f503b">IWICDevelopRawNotificationCallback</a>*</b>

Pointer to the notification callback method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



