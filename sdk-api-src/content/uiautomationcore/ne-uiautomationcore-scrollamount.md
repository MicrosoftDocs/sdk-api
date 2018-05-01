---
UID: NE:uiautomationcore.ScrollAmount
title: ScrollAmount
author: windows-driver-content
description: Contains values that specify the direction and distance to scroll.
old-location: winauto\uiauto_ScrollAmount.htm
old-project: WinAuto
ms.assetid: 94d84a66-5222-48e4-9675-444eb04558a4
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ScrollAmount, ScrollAmount enumeration [Windows Accessibility], ScrollAmount_LargeDecrement, ScrollAmount_LargeIncrement, ScrollAmount_NoAmount, ScrollAmount_SmallDecrement, ScrollAmount_SmallIncrement, uiauto.uiauto_ScrollAmount, uiauto_ScrollAmount, uiautomationcore/ScrollAmount, uiautomationcore/ScrollAmount_LargeDecrement, uiautomationcore/ScrollAmount_LargeIncrement, uiautomationcore/ScrollAmount_NoAmount, uiautomationcore/ScrollAmount_SmallDecrement, uiautomationcore/ScrollAmount_SmallIncrement, winauto.uiauto_ScrollAmount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	UIAutomationCore.h
api_name:
-	ScrollAmount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ScrollAmount enumeration


## -description


Contains values that specify the direction and distance to scroll.


## -enum-fields




### -field ScrollAmount_LargeDecrement

Scrolling is done in large decrements, equivalent to pressing the PAGE UP key or clicking on a blank part of a scroll bar. If one page up is not a relevant amount for the control and no scroll bar exists, the value represents an amount equal to the current visible window.


### -field ScrollAmount_SmallDecrement

Scrolling is done in small decrements, equivalent to pressing an arrow key or clicking the arrow button on a scroll bar.


### -field ScrollAmount_NoAmount

No scrolling is done. 


### -field ScrollAmount_LargeIncrement

Scrolling is done in large increments, equivalent to pressing the PAGE DOWN or PAGE UP key or clicking on a blank part of a scroll bar. 
			If one page is not a relevant amount for the control and no scroll bar exists, the value represents an amount equal to the current visible window.


### -field ScrollAmount_SmallIncrement

Scrolling is done in small increments, equivalent to pressing an arrow key or clicking the arrow 
			button on a scroll bar.


## -see-also




<a href="https://msdn.microsoft.com/55e1b899-aa9f-45eb-9cfa-d645ea659988">IScrollProvider</a>
 

 

