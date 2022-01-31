---
UID: NE:wincodec.WICProgressOperation
title: WICProgressOperation (wincodec.h)
description: Specifies the progress operations to receive notifications for.
helpviewer_keywords: ["WICProgressOperation","WICProgressOperation enumeration [Windows Imaging Component]","WICProgressOperationAll","WICProgressOperationCopyPixels","WICProgressOperationWritePixels","_wic_codec_wicprogressoperation","wic._wic_codec_wicprogressoperation","wincodec/WICProgressOperation","wincodec/WICProgressOperationAll","wincodec/WICProgressOperationCopyPixels","wincodec/WICProgressOperationWritePixels"]
old-location: wic\_wic_codec_wicprogressoperation.htm
tech.root: wic
ms.assetid: 407b982d-7232-42ce-9ff5-7029b7d922a4
ms.date: 12/05/2018
ms.keywords: WICProgressOperation, WICProgressOperation enumeration [Windows Imaging Component], WICProgressOperationAll, WICProgressOperationCopyPixels, WICProgressOperationWritePixels, _wic_codec_wicprogressoperation, wic._wic_codec_wicprogressoperation, wincodec/WICProgressOperation, wincodec/WICProgressOperationAll, wincodec/WICProgressOperationCopyPixels, wincodec/WICProgressOperationWritePixels
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICProgressOperation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICProgressOperation
 - wincodec/WICProgressOperation
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
 - WICProgressOperation
---

# WICProgressOperation enumeration


## -description

Specifies the progress operations to receive notifications for.

## -enum-fields

### -field WICProgressOperationCopyPixels:0x1

Receive copy pixel operation.

### -field WICProgressOperationWritePixels:0x2

Receive write pixel operation.

### -field WICProgressOperationAll:0xffff

Receive all progress operations available.

### -field WICPROGRESSOPERATION_FORCE_DWORD:0x7fffffff

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification">RegisterProgressNotification</a>
