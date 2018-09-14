---
UID: NE:wincodec.WICProgressNotification
title: WICProgressNotification
author: windows-sdk-content
description: Specifies when the progress notification callback should be called.
old-location: wic\_wic_codec_wicprogressnotification.htm
tech.root: wic
ms.assetid: 6d7ef6f1-2024-4de5-9c2e-8edc6359f79b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: WICProgressNotification, WICProgressNotification enumeration [Windows Imaging Component], WICProgressNotificationAll, WICProgressNotificationBegin, WICProgressNotificationEnd, WICProgressNotificationFrequent, _wic_codec_wicprogressnotification, wic._wic_codec_wicprogressnotification, wincodec/WICProgressNotification, wincodec/WICProgressNotificationAll, wincodec/WICProgressNotificationBegin, wincodec/WICProgressNotificationEnd, wincodec/WICProgressNotificationFrequent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICProgressNotification
product: Windows
targetos: Windows
req.typenames: WICProgressNotification
req.redist: 
---

# WICProgressNotification enumeration


## -description


Specifies when the progress notification callback should be called.


## -enum-fields




### -field WICProgressNotificationBegin

The callback should be called when codec operations begin.


### -field WICProgressNotificationEnd

The callback should be called when codec operations end.


### -field WICProgressNotificationFrequent

The callback should be called frequently to report status.


### -field WICProgressNotificationAll

The callback should be called on all available progress notifications.


### -field WICPROGRESSNOTIFICATION_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/ac47178a-f149-4313-8673-ece59e88cfb3">RegisterProgressNotification</a>
 

 

