---
UID: NF:msinkaut.IInkOverlay.put_SupportHighContrastSelectionUI
title: IInkOverlay::put_SupportHighContrastSelectionUI
author: windows-sdk-content
description: Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode.
old-location: tablet\inkoverlay_supporthighcontrastselectionui.htm
old-project: tablet
ms.assetid: a8837657-6eb0-44d3-8c39-11a5524fe9db
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IInkOverlay, IInkOverlay interface [Tablet PC],SupportHighContrastSelectionUI property, IInkOverlay.SupportHighContrastSelectionUI, IInkOverlay.put_SupportHighContrastSelectionUI, IInkOverlay::SupportHighContrastSelectionUI, IInkOverlay::get_SupportHighContrastSelectionUI, IInkOverlay::put_SupportHighContrastSelectionUI, InkOverlay.get_SupportHighContrastSelectionUI, InkOverlay.put_SupportHighContrastSelectionUI, SupportHighContrastSelectionUI property [Tablet PC], SupportHighContrastSelectionUI property [Tablet PC],IInkOverlay interface, a8837657-6eb0-44d3-8c39-11a5524fe9db, msinkaut/IInkOverlay::SupportHighContrastSelectionUI, msinkaut/IInkOverlay::get_SupportHighContrastSelectionUI, msinkaut/IInkOverlay::put_SupportHighContrastSelectionUI, put_SupportHighContrastSelectionUI, tablet.inkoverlay_supporthighcontrastselectionui
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkOverlay.SupportHighContrastSelectionUI
-	IInkOverlay.get_SupportHighContrastSelectionUI
-	IInkOverlay.put_SupportHighContrastSelectionUI
-	InkOverlay.get_SupportHighContrastSelectionUI
-	InkOverlay.put_SupportHighContrastSelectionUI
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::put_SupportHighContrastSelectionUI


## -description



Gets or sets a value that specifies whether all selection user interface (UI) elements are drawn in high contrast when the system is in High Contrast mode.



This property is read/write.


## -parameters


## -remarks



This property changes the way selection UI is displayed when the system changes to High Contrast mode. Selection UI elements include the selection bounding box and the selection handles.

Ink selection uses the COLOR_WINDOWTEXT, COLOR_WINDOW, and COLOR_HIGHLIGHT system colors to draw elements of the selection UI when the system is in High Contrast mode and the <b>SupportHighContrastSelectionUI</b> property is <b>TRUE</b>. For more information on system colors, see the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function in MSDN.




## -see-also




<a href="https://msdn.microsoft.com/885ace6d-952e-4870-b92c-92e47daadfcf">Color Property</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/17f5002b-0191-4cb0-8b12-0383aaabe2a8">SupportHighContrastInk Property</a>
 

 

