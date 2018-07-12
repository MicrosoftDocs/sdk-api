---
UID: NF:msinkaut.IInkOverlay.get_EditingMode
title: IInkOverlay::get_EditingMode
author: windows-sdk-content
description: Gets or sets a value that specifies whether the object/control is in ink mode, deletion mode, or selecting/editing mode.
old-location: tablet\inkoverlay_editingmode.htm
old-project: tablet
ms.assetid: 3b734da3-5784-4504-b22e-b86844d42f4e
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: 3b734da3-5784-4504-b22e-b86844d42f4e, EditingMode property [Tablet PC], EditingMode property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],EditingMode property, IInkOverlay.EditingMode, IInkOverlay.get_EditingMode, IInkOverlay::EditingMode, IInkOverlay::get_EditingMode, IInkOverlay::put_EditingMode, InkOverlay.get_EditingMode, InkOverlay.put_EditingMode, get_EditingMode, msinkaut/IInkOverlay::EditingMode, msinkaut/IInkOverlay::get_EditingMode, msinkaut/IInkOverlay::put_EditingMode, put_EditingMode, tablet.inkoverlay_editingmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.EditingMode
 - IInkOverlay.get_EditingMode
 - IInkOverlay.put_EditingMode
 - InkOverlay.get_EditingMode
 - InkOverlay.put_EditingMode
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

