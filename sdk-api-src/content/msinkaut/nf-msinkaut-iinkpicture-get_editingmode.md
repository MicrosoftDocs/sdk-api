---
UID: NF:msinkaut.IInkPicture.get_EditingMode
title: IInkPicture::get_EditingMode
author: windows-sdk-content
description: Gets or sets a value that specifies whether the InkPicture control is in ink mode, deletion mode, or selecting/editing mode.
old-location: tablet\inkpicture_editingmode.htm
tech.root: tablet
ms.assetid: 5767f768-d59c-404e-9098-ab5e0c427c7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5767f768-d59c-404e-9098-ab5e0c427c7d, EditingMode property [Tablet PC], EditingMode property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],EditingMode property, IInkPicture.EditingMode, IInkPicture.get_EditingMode, IInkPicture::EditingMode, IInkPicture::get_EditingMode, IInkPicture::put_EditingMode, InkPicture.get_EditingMode, InkPicture.put_EditingMode, get_EditingMode, msinkaut/IInkPicture::EditingMode, msinkaut/IInkPicture::get_EditingMode, msinkaut/IInkPicture::put_EditingMode, put_EditingMode, tablet.inkpicture_editingmode
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkPicture.EditingMode
 - IInkPicture.get_EditingMode
 - IInkPicture.put_EditingMode
 - InkPicture.get_EditingMode
 - InkPicture.put_EditingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkPicture::get_EditingMode


## -description



Gets or sets a value that specifies whether the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.



This property is read/write.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> and <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> objects generate an error if you change the <b>EditingMode</b> property while ink is being collected. To avoid this conflict, make sure the <a href="https://msdn.microsoft.com/19fbe26e-02a4-4d05-a2e8-25d2f8ae1146">CollectingInk</a> property is <b>FALSE</b> before changing the <b>EditingMode</b> property.

For more information about erasing ink, see <a href="https://msdn.microsoft.com/9851c871-4d1c-43b6-9615-5d231cbc01ae">Erasing Ink with the Pen</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

