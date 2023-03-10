---
UID: NE:wincodec.WICProgressNotification
title: WICProgressNotification (wincodec.h)
description: Specifies when the progress notification callback should be called.
helpviewer_keywords: ["WICProgressNotification","WICProgressNotification enumeration [Windows Imaging Component]","WICProgressNotificationAll","WICProgressNotificationBegin","WICProgressNotificationEnd","WICProgressNotificationFrequent","_wic_codec_wicprogressnotification","wic._wic_codec_wicprogressnotification","wincodec/WICProgressNotification","wincodec/WICProgressNotificationAll","wincodec/WICProgressNotificationBegin","wincodec/WICProgressNotificationEnd","wincodec/WICProgressNotificationFrequent"]
old-location: wic\_wic_codec_wicprogressnotification.htm
tech.root: wic
ms.assetid: 6d7ef6f1-2024-4de5-9c2e-8edc6359f79b
ms.date: 12/05/2018
ms.keywords: WICProgressNotification, WICProgressNotification enumeration [Windows Imaging Component], WICProgressNotificationAll, WICProgressNotificationBegin, WICProgressNotificationEnd, WICProgressNotificationFrequent, _wic_codec_wicprogressnotification, wic._wic_codec_wicprogressnotification, wincodec/WICProgressNotification, wincodec/WICProgressNotificationAll, wincodec/WICProgressNotificationBegin, wincodec/WICProgressNotificationEnd, wincodec/WICProgressNotificationFrequent
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
targetos: Windows
req.typenames: WICProgressNotification
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICProgressNotification
 - wincodec/WICProgressNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICProgressNotification
---

# WICProgressNotification enumeration


## -description

Specifies when the progress notification callback should be called.

## -enum-fields

### -field WICProgressNotificationBegin:0x10000

The callback should be called when codec operations begin.

### -field WICProgressNotificationEnd:0x20000

The callback should be called when codec operations end.

### -field WICProgressNotificationFrequent:0x40000

The callback should be called frequently to report status.

### -field WICProgressNotificationAll:0xffff0000

The callback should be called on all available progress notifications.

### -field WICPROGRESSNOTIFICATION_FORCE_DWORD:0x7fffffff

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification">RegisterProgressNotification</a>
