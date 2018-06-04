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

# IInkPicture::put_SizeMode


## -description


Gets or sets how the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control handles image placement and sizing.


This property is read/write.


## -parameters


## -remarks



Valid values for this property are taken from the <a href="https://msdn.microsoft.com/e24c38b4-b25f-4d0e-88f5-f56f5dc6be1a">InkPictureSizeMode</a> enumeration. By default, in <b>IPSM_Normal</b> mode, the picture is positioned in the upper-left corner of the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control, and any part of the image too big for the InkPicture control is clipped. Using the <b>IPSM_StretchImage</b> value causes the picture to stretch to fit the control.



Using the <b>IPSM_AutoSize</b> value causes the control to resize to always fit the picture. Using the <b>IPSM_CenterImage</b> value causes the picture to be centered in the control.






## -see-also




<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/e24c38b4-b25f-4d0e-88f5-f56f5dc6be1a">InkPictureSizeMode</a>
 

 

