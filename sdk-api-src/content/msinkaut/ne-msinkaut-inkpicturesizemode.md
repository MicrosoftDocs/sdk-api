---
UID: NE:msinkaut.InkPictureSizeMode
title: InkPictureSizeMode (msinkaut.h)
description: Specifies how the picture behaves inside the InkPicture control.
helpviewer_keywords: ["IPSM_AutoSize","IPSM_CenterImage","IPSM_Normal","IPSM_StretchImage","InkPictureSizeMode","InkPictureSizeMode enumeration [Tablet PC]","e24c38b4-b25f-4d0e-88f5-f56f5dc6be1a","msinkaut/IPSM_AutoSize","msinkaut/IPSM_CenterImage","msinkaut/IPSM_Normal","msinkaut/IPSM_StretchImage","msinkaut/InkPictureSizeMode","tablet.inkpicturesizemode"]
old-location: tablet\inkpicturesizemode.htm
tech.root: tablet
ms.assetid: e24c38b4-b25f-4d0e-88f5-f56f5dc6be1a
ms.date: 12/05/2018
ms.keywords: IPSM_AutoSize, IPSM_CenterImage, IPSM_Normal, IPSM_StretchImage, InkPictureSizeMode, InkPictureSizeMode enumeration [Tablet PC], e24c38b4-b25f-4d0e-88f5-f56f5dc6be1a, msinkaut/IPSM_AutoSize, msinkaut/IPSM_CenterImage, msinkaut/IPSM_Normal, msinkaut/IPSM_StretchImage, msinkaut/InkPictureSizeMode, tablet.inkpicturesizemode
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
req.typenames: InkPictureSizeMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkPictureSizeMode
 - msinkaut/InkPictureSizeMode
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
 - InkPictureSizeMode
---

# InkPictureSizeMode enumeration


## -description

Specifies how the picture behaves inside the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.
          
        

The mode is set by using the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode">SizeMode</a> property and is applied to the picture set with the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture">Picture</a> property.

## -enum-fields

### -field IPSM_AutoSize:0

The control auto sizes to fit the picture.

### -field IPSM_CenterImage:1

The picture is centered within the control.

### -field IPSM_Normal:2

The picture appears at its regular size within the control.

### -field IPSM_StretchImage:3

 The picture is stretched within the control.

## -see-also

<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>
