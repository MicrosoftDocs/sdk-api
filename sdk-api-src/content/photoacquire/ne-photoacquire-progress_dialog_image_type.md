---
UID: NE:photoacquire.tagPROGRESS_DIALOG_IMAGE_TYPE
title: PROGRESS_DIALOG_IMAGE_TYPE (photoacquire.h)
description: The PROGRESS_DIALOG_IMAGE_TYPE enumeration type indicates the image type set in IPhotoProgressDialog::SetImage.
helpviewer_keywords: ["PROGRESS_DIALOG_BITMAP_THUMBNAIL","PROGRESS_DIALOG_ICON_LARGE","PROGRESS_DIALOG_ICON_SMALL","PROGRESS_DIALOG_ICON_THUMBNAIL","PROGRESS_DIALOG_IMAGE_TYPE","PROGRESS_DIALOG_IMAGE_TYPE enumeration [Picture Acquisition]","enumeration [Picture Acquisition]","photoacquire/PROGRESS_DIALOG_BITMAP_THUMBNAIL","photoacquire/PROGRESS_DIALOG_ICON_LARGE","photoacquire/PROGRESS_DIALOG_ICON_SMALL","photoacquire/PROGRESS_DIALOG_ICON_THUMBNAIL","photoacquire/PROGRESS_DIALOG_IMAGE_TYPE","picacq.progress_dialog_image_type"]
old-location: picacq\progress_dialog_image_type.htm
tech.root: picacq
ms.assetid: 05da00c6-e8de-4482-ab2c-f1b969cfa877
ms.date: 12/05/2018
ms.keywords: PROGRESS_DIALOG_BITMAP_THUMBNAIL, PROGRESS_DIALOG_ICON_LARGE, PROGRESS_DIALOG_ICON_SMALL, PROGRESS_DIALOG_ICON_THUMBNAIL, PROGRESS_DIALOG_IMAGE_TYPE, PROGRESS_DIALOG_IMAGE_TYPE enumeration [Picture Acquisition], enumeration [Picture Acquisition], photoacquire/PROGRESS_DIALOG_BITMAP_THUMBNAIL, photoacquire/PROGRESS_DIALOG_ICON_LARGE, photoacquire/PROGRESS_DIALOG_ICON_SMALL, photoacquire/PROGRESS_DIALOG_ICON_THUMBNAIL, photoacquire/PROGRESS_DIALOG_IMAGE_TYPE, picacq.progress_dialog_image_type
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: PROGRESS_DIALOG_IMAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPROGRESS_DIALOG_IMAGE_TYPE
 - photoacquire/tagPROGRESS_DIALOG_IMAGE_TYPE
 - PROGRESS_DIALOG_IMAGE_TYPE
 - photoacquire/PROGRESS_DIALOG_IMAGE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PhotoAcquire.h
api_name:
 - PROGRESS_DIALOG_IMAGE_TYPE
---

# PROGRESS_DIALOG_IMAGE_TYPE enumeration


## -description

The <code>PROGRESS_DIALOG_IMAGE_TYPE</code> enumeration type indicates the image type set in <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setimage">IPhotoProgressDialog::SetImage</a>.

## -enum-fields

### -field PROGRESS_DIALOG_ICON_SMALL:0

Specifies the small icon used in the title bar (normally 16 x 16 pixels).

### -field PROGRESS_DIALOG_ICON_LARGE:0x1

Specifies the icon used to represent the progress dialog box in ALT+TAB key combination windows (normally 32 x 32 pixels).

### -field PROGRESS_DIALOG_ICON_THUMBNAIL:0x2

Specifies an icon used in place of the thumbnail (up to 128 x 128 pixels).

### -field PROGRESS_DIALOG_BITMAP_THUMBNAIL:0x3

Specifies a bitmap thumbnail (up to 128 x 128 pixels, although it will be scaled to fit if it is too large).

## -see-also

<a href="/previous-versions/windows/desktop/acquisition/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoprogressdialog-setimage">IPhotoAcquireProgressDialog::SetImage</a>
