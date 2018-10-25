---
UID: NF:msinkaut.IInkCollector.get_SupportHighContrastInk
title: IInkCollector::get_SupportHighContrastInk
author: windows-sdk-content
description: Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.
old-location: tablet\inkcollector_supporthighcontrastink.htm
tech.root: tablet
ms.assetid: 17f5002b-0191-4cb0-8b12-0383aaabe2a8
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 17f5002b-0191-4cb0-8b12-0383aaabe2a8, IInkCollector interface [Tablet PC],SupportHighContrastInk property, IInkCollector.SupportHighContrastInk, IInkCollector.get_SupportHighContrastInk, IInkCollector::SupportHighContrastInk, IInkCollector::get_SupportHighContrastInk, IInkCollector::put_SupportHighContrastInk, InkCollector.get_SupportHighContrastInk, InkCollector.put_SupportHighContrastInk, SupportHighContrastInk property [Tablet PC], SupportHighContrastInk property [Tablet PC],IInkCollector interface, get_SupportHighContrastInk, msinkaut/IInkCollector::SupportHighContrastInk, msinkaut/IInkCollector::get_SupportHighContrastInk, msinkaut/IInkCollector::put_SupportHighContrastInk, put_SupportHighContrastInk, tablet.inkcollector_supporthighcontrastink
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
 - IInkCollector.SupportHighContrastInk
 - IInkCollector.get_SupportHighContrastInk
 - IInkCollector.put_SupportHighContrastInk
 - InkCollector.get_SupportHighContrastInk
 - InkCollector.put_SupportHighContrastInk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCollector::get_SupportHighContrastInk


## -description



Gets or sets a value that specifies whether ink is rendered as just one color when the system is in High Contrast mode.



This property is read/write.


## -parameters


## -remarks



This property changes the way ink renders when the system changes to High Contrast mode.

Real-time ink application uses the COLOR_WINDOWTEXT color when the system is in High Contrast mode and the <b>SupportHighContrastInk</b> property is <b>TRUE</b>, but the inherent color of a stroke made under these conditions remains unchanged. For example, if the <a href="https://msdn.microsoft.com/885ace6d-952e-4870-b92c-92e47daadfcf">Color</a> property is set to <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB(0,0,255)</a> (blue), the COLOR_WINDOWTEXT color is set to RGB(255,255,255) (white), and the system is in High Contrast mode, then a newly drawn stroke renders in white but the actual stroke color is still blue. For more information about this behavior, see the <b>Color</b> property and the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function.




## -see-also




<a href="https://msdn.microsoft.com/885ace6d-952e-4870-b92c-92e47daadfcf">Color Property</a>



<a href="https://msdn.microsoft.com/f31a93aa-e3de-4254-af3f-338576350815">DefaultDrawingAttributes Property</a>



<a href="https://msdn.microsoft.com/4E539E4F-2E7F-44ED-A8D0-650BCAFDFAFB">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/a8837657-6eb0-44d3-8c39-11a5524fe9db">SupportHighContrastSelectionUI Property [InkOverlay Class]</a>
 

 

