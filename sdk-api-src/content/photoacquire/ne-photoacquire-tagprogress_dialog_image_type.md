---
UID: NE:photoacquire.tagPROGRESS_DIALOG_IMAGE_TYPE
title: tagPROGRESS_DIALOG_IMAGE_TYPE
author: windows-driver-content
description: The PROGRESS_DIALOG_IMAGE_TYPE enumeration type indicates the image type set in IPhotoProgressDialog::SetImage.
old-location: picacq\progress_dialog_image_type.htm
old-project: acquisition
ms.assetid: 05da00c6-e8de-4482-ab2c-f1b969cfa877
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PROGRESS_DIALOG_BITMAP_THUMBNAIL, PROGRESS_DIALOG_ICON_LARGE, PROGRESS_DIALOG_ICON_SMALL, PROGRESS_DIALOG_ICON_THUMBNAIL, PROGRESS_DIALOG_IMAGE_TYPE, PROGRESS_DIALOG_IMAGE_TYPE enumeration [Picture Acquisition], enumeration [Picture Acquisition], photoacquire/PROGRESS_DIALOG_BITMAP_THUMBNAIL, photoacquire/PROGRESS_DIALOG_ICON_LARGE, photoacquire/PROGRESS_DIALOG_ICON_SMALL, photoacquire/PROGRESS_DIALOG_ICON_THUMBNAIL, photoacquire/PROGRESS_DIALOG_IMAGE_TYPE, picacq.progress_dialog_image_type, tagPROGRESS_DIALOG_IMAGE_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: PROGRESS_DIALOG_IMAGE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PhotoAcquire.h
api_name:
-	PROGRESS_DIALOG_IMAGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# tagPROGRESS_DIALOG_IMAGE_TYPE enumeration


## -description



The <code>PROGRESS_DIALOG_IMAGE_TYPE</code> enumeration type indicates the image type set in <a href="https://msdn.microsoft.com/45b795c4-4f95-4132-86a7-cda47e534e9c">IPhotoProgressDialog::SetImage</a>.




## -enum-fields




### -field PROGRESS_DIALOG_ICON_SMALL

Specifies the small icon used in the title bar (normally 16 x 16 pixels).


### -field PROGRESS_DIALOG_ICON_LARGE

Specifies the icon used to represent the progress dialog box in ALT+TAB key combination windows (normally 32 x 32 pixels).


### -field PROGRESS_DIALOG_ICON_THUMBNAIL

Specifies an icon used in place of the thumbnail (up to 128 x 128 pixels).


### -field PROGRESS_DIALOG_BITMAP_THUMBNAIL

Specifies a bitmap thumbnail (up to 128 x 128 pixels, although it will be scaled to fit if it is too large).


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/45b795c4-4f95-4132-86a7-cda47e534e9c">IPhotoAcquireProgressDialog::SetImage</a>
 

 

