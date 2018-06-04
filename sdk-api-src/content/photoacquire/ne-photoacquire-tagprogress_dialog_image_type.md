---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

