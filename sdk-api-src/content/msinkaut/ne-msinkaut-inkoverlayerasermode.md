---
UID: NE:msinkaut.InkOverlayEraserMode
title: InkOverlayEraserMode (msinkaut.h)
description: Specifies the way in which ink is erased from the InkOverlay object and the InkPicture control.This mode is used when the InkOverlayEditingMode is set to Delete.
helpviewer_keywords: ["IOERM_PointErase","IOERM_StrokeErase","InkOverlayEraserMode","InkOverlayEraserMode enumeration [Tablet PC]","e7400a40-9b82-4750-8e92-a39c6f25b7cd","msinkaut/IOERM_PointErase","msinkaut/IOERM_StrokeErase","msinkaut/InkOverlayEraserMode","tablet.inkoverlayerasermode"]
old-location: tablet\inkoverlayerasermode.htm
tech.root: tablet
ms.assetid: e7400a40-9b82-4750-8e92-a39c6f25b7cd
ms.date: 12/05/2018
ms.keywords: IOERM_PointErase, IOERM_StrokeErase, InkOverlayEraserMode, InkOverlayEraserMode enumeration [Tablet PC], e7400a40-9b82-4750-8e92-a39c6f25b7cd, msinkaut/IOERM_PointErase, msinkaut/IOERM_StrokeErase, msinkaut/InkOverlayEraserMode, tablet.inkoverlayerasermode
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
req.typenames: InkOverlayEraserMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkOverlayEraserMode
 - msinkaut/InkOverlayEraserMode
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
 - InkOverlayEraserMode
---

# InkOverlayEraserMode enumeration


## -description

Specifies the way in which ink is erased from the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object and the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

This mode is used when the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode">InkOverlayEditingMode</a> is set to Delete.

## -enum-fields

### -field IOERM_StrokeErase:0

 Ink is erased by stroke.

This is the default value.

### -field IOERM_PointErase:1

Ink is erased by point.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode">EraserMode Property [InkPicture Control]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth">EraserWidth Property [InkPicture Control]</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode">InkOverlayEditingMode Enumeration</a>
