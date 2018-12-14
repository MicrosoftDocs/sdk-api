---
UID: NF:msinkaut.IInkOverlay.get_SupportHighContrastInk
title: IInkOverlay::get_SupportHighContrastInk
author: windows-sdk-content
description: Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.
old-location: tablet\inkoverlay_supporthighcontrastink.htm
tech.root: tablet
ms.assetid: 69c0c628-e377-4c26-8fb7-1f0574fbff29
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInkOverlay interface [Tablet PC],SupportHighContrastInk property, IInkOverlay.SupportHighContrastInk, IInkOverlay.get_SupportHighContrastInk, IInkOverlay::SupportHighContrastInk, IInkOverlay::get_SupportHighContrastInk, IInkOverlay::put_SupportHighContrastInk, InkOverlay.get_SupportHighContrastInk, InkOverlay.put_SupportHighContrastInk, SupportHighContrastInk property [Tablet PC], SupportHighContrastInk property [Tablet PC],IInkOverlay interface, get_SupportHighContrastInk, msinkaut/IInkOverlay::SupportHighContrastInk, msinkaut/IInkOverlay::get_SupportHighContrastInk, msinkaut/IInkOverlay::put_SupportHighContrastInk, put_SupportHighContrastInk, tablet.inkoverlay_supporthighcontrastink
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
 - IInkOverlay.SupportHighContrastInk
 - IInkOverlay.get_SupportHighContrastInk
 - IInkOverlay.put_SupportHighContrastInk
 - InkOverlay.get_SupportHighContrastInk
 - InkOverlay.put_SupportHighContrastInk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkOverlay::get_SupportHighContrastInk


## -description



Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.



This property is read/write.


## -parameters


## -remarks



This property changes the way ink renders when the system changes to High Contrast mode.

Real-time ink application uses the COLOR_WINDOWTEXT color when the system is in High Contrast mode and the <a href="https://msdn.microsoft.com/17f5002b-0191-4cb0-8b12-0383aaabe2a8">SupportHighContrastInk</a> property is <b>TRUE</b>, but the inherent color of a stroke made under these conditions remains unchanged. For example, if the <a href="https://msdn.microsoft.com/885ace6d-952e-4870-b92c-92e47daadfcf">Color</a> property is set to <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB(0,0,255)</a> (blue), the COLOR_WINDOWTEXT color is set to RGB(255,255,255) (white), and the system is in High Contrast mode, then a newly drawn stroke renders in white but the actual stroke color is still blue. For more information about this behavior, see the <b>Color</b> property and the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function.




## -see-also




<a href="https://msdn.microsoft.com/885ace6d-952e-4870-b92c-92e47daadfcf">Color Property</a>



<a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846799(v=VS.85).aspx">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/a8837657-6eb0-44d3-8c39-11a5524fe9db">SupportHighContrastSelectionUI Property [InkOverlay Class]</a>
 

 

