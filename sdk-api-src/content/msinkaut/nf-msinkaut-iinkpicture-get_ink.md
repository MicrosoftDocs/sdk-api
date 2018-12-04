---
UID: NF:msinkaut.IInkPicture.get_Ink
title: IInkPicture::get_Ink
author: windows-sdk-content
description: Gets or sets the InkDisp object that is associated with the InkPicture control.
old-location: tablet\inkpicture_ink.htm
tech.root: tablet
ms.assetid: 8a6001bb-cfb9-4c24-8f99-3c8f0acd443c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 8a6001bb-cfb9-4c24-8f99-3c8f0acd443c, IInkPicture interface [Tablet PC],Ink property, IInkPicture.Ink, IInkPicture.get_Ink, IInkPicture::Ink, IInkPicture::get_Ink, IInkPicture::put_Ink, Ink property [Tablet PC], Ink property [Tablet PC],IInkPicture interface, InkPicture.get_Ink, InkPicture.put_Ink, get_Ink, get_ink, msinkaut/IInkPicture::Ink, msinkaut/IInkPicture::get_Ink, msinkaut/IInkPicture::put_Ink, putref_ink, tablet.inkpicture_ink
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IInkPicture.Ink
 - IInkPicture.get_Ink
 - IInkPicture.put_Ink
 - InkPicture.get_Ink
 - InkPicture.put_Ink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkPicture::get_Ink


## -description



Gets or sets the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that is associated with the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control must be disabled before setting this property. To disable inking in the InkPicture control, set the <a href="https://msdn.microsoft.com/3af59de9-0239-47ab-b3b3-1f1baecb169f">InkEnabled</a> property to <b>FALSE</b>. You can then set the <b>Ink</b> property, and re-enable the control by setting the <b>InkEnabled</b> property to <b>TRUE</b>.</div>
<div> </div>
For further details about this property, refer to the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object's <a href="https://msdn.microsoft.com/66b7e5fd-c20b-465d-80dd-31d4d714d00d">Ink</a> property, which has the same functionality.




## -see-also




<a href="https://msdn.microsoft.com/EA6AC3DD-5F13-442A-B93D-FF0A5333609A">IInkPicture</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

