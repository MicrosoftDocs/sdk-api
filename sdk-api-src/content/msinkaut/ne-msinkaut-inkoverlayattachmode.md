---
UID: NE:msinkaut.InkOverlayAttachMode
title: InkOverlayAttachMode (msinkaut.h)
description: Specifies where to attach the new InkOverlay object, behind or in front of the active layer.
helpviewer_keywords: ["5b46c6fc-2415-4ed2-a2f9-47a6e8455ff0","IOAM_Behind","IOAM_InFront","InkOverlayAttachMode","InkOverlayAttachMode enumeration [Tablet PC]","msinkaut/IOAM_Behind","msinkaut/IOAM_InFront","msinkaut/InkOverlayAttachMode","tablet.inkoverlayattachmode"]
old-location: tablet\inkoverlayattachmode.htm
tech.root: tablet
ms.assetid: 5b46c6fc-2415-4ed2-a2f9-47a6e8455ff0
ms.date: 12/05/2018
ms.keywords: 5b46c6fc-2415-4ed2-a2f9-47a6e8455ff0, IOAM_Behind, IOAM_InFront, InkOverlayAttachMode, InkOverlayAttachMode enumeration [Tablet PC], msinkaut/IOAM_Behind, msinkaut/IOAM_InFront, msinkaut/InkOverlayAttachMode, tablet.inkoverlayattachmode
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: InkOverlayAttachMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkOverlayAttachMode
 - msinkaut/InkOverlayAttachMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkOverlayAttachMode
---

# InkOverlayAttachMode enumeration


## -description

Specifies where to attach the new <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, behind or in front of the active layer.

## -enum-fields

### -field IOAM_Behind:0

The new <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is attached behind the active window.

This is the default value.

### -field IOAM_InFront:1

The new <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is attached in front of the active window.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode">AttachMode Property</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
