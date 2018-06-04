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

# IInkOverlay::get_EditingMode


## -description



Gets or sets a value that specifies whether the object/control is in ink mode, deletion mode, or selecting/editing mode.



This property is read/write.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> and <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> objects generate an error if you change the <b>EditingMode</b> property while ink is being collected. To avoid this conflict, make sure the <a href="https://msdn.microsoft.com/c0ac36a8-e36e-45a7-b047-14d7f7c8ce14">CollectingInk</a> property is <b>FALSE</b> before changing the <b>EditingMode</b> property.

For more information about erasing ink, see <a href="https://msdn.microsoft.com/9851c871-4d1c-43b6-9615-5d231cbc01ae">Erasing Ink with the Pen</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/3af59de9-0239-47ab-b3b3-1f1baecb169f">InkEnabled Property</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/de25636c-b8ca-47e4-ae16-182b98ede8f6">InkOverlayEditingMode Enumeration</a>
 

 

