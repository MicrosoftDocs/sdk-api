---
UID: NF:msinkaut.IInkPicture.get_SupportHighContrastInk
title: IInkPicture::get_SupportHighContrastInk
author: windows-sdk-content
description: Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.
old-location: tablet\inkpicture_supporthighcontrastink.htm
old-project: tablet
ms.assetid: 9f57e1fe-8224-43ef-bd26-2d15da625725
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IInkPicture interface [Tablet PC],SupportHighContrastInk property, IInkPicture.SupportHighContrastInk, IInkPicture.get_SupportHighContrastInk, IInkPicture::SupportHighContrastInk, IInkPicture::get_SupportHighContrastInk, IInkPicture::put_SupportHighContrastInk, InkPicture.get_SupportHighContrastInk, InkPicture.put_SupportHighContrastInk, SupportHighContrastInk property [Tablet PC], SupportHighContrastInk property [Tablet PC],IInkPicture interface, get_SupportHighContrastInk, msinkaut/IInkPicture::SupportHighContrastInk, msinkaut/IInkPicture::get_SupportHighContrastInk, msinkaut/IInkPicture::put_SupportHighContrastInk, putt_SupportHighContrastInk, tablet.inkpicture_supporthighcontrastink
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
 - IInkPicture.SupportHighContrastInk
 - IInkPicture.get_SupportHighContrastInk
 - IInkPicture.put_SupportHighContrastInk
 - InkPicture.get_SupportHighContrastInk
 - InkPicture.put_SupportHighContrastInk
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::get_SupportHighContrastInk


## -description



Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.



This property is read/write.


## -parameters


## -remarks



This property changes the way ink renders when the system changes to High Contrast mode.

Real-time ink application uses the COLOR_WINDOWTEXT color when the system is in High Contrast mode and the <b>SupportHighContrastInk</b> property is <b>TRUE</b>, but the inherent color of a stroke made under these conditions remains unchanged. For example, if the <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> property is set to <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB(0,0,255)</a> (blue), the COLOR_WINDOWTEXT color is set to RGB(255,255,255) (white), and the system is in High Contrast mode, then a newly drawn stroke renders in white but the actual stroke color is still blue. For more information about this behavior, see the <b>Color</b> property and the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function.




## -see-also




<a href="https://msdn.microsoft.com/885ace6d-952e-4870-b92c-92e47daadfcf">Color Property</a>



<a href="https://msdn.microsoft.com/9a4dff66-9789-4979-947e-73bbf85cece2">DefaultDrawingAttributes Property</a>



<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/f522a998-89f0-4d8d-bb19-949d62f5a786">SupportHighContrastSelectionUI Property [InkPicture Control]</a>
 

 

