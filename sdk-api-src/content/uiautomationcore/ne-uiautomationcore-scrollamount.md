---
UID: NE:uiautomationcore.ScrollAmount
title: ScrollAmount (uiautomationcore.h)
description: Contains values that specify the direction and distance to scroll.
helpviewer_keywords: ["ScrollAmount","ScrollAmount enumeration [Windows Accessibility]","ScrollAmount_LargeDecrement","ScrollAmount_LargeIncrement","ScrollAmount_NoAmount","ScrollAmount_SmallDecrement","ScrollAmount_SmallIncrement","uiauto.uiauto_ScrollAmount","uiauto_ScrollAmount","uiautomationcore/ScrollAmount","uiautomationcore/ScrollAmount_LargeDecrement","uiautomationcore/ScrollAmount_LargeIncrement","uiautomationcore/ScrollAmount_NoAmount","uiautomationcore/ScrollAmount_SmallDecrement","uiautomationcore/ScrollAmount_SmallIncrement","winauto.uiauto_ScrollAmount"]
old-location: winauto\uiauto_ScrollAmount.htm
tech.root: WinAuto
ms.assetid: 94d84a66-5222-48e4-9675-444eb04558a4
ms.date: 12/05/2018
ms.keywords: ScrollAmount, ScrollAmount enumeration [Windows Accessibility], ScrollAmount_LargeDecrement, ScrollAmount_LargeIncrement, ScrollAmount_NoAmount, ScrollAmount_SmallDecrement, ScrollAmount_SmallIncrement, uiauto.uiauto_ScrollAmount, uiauto_ScrollAmount, uiautomationcore/ScrollAmount, uiautomationcore/ScrollAmount_LargeDecrement, uiautomationcore/ScrollAmount_LargeIncrement, uiautomationcore/ScrollAmount_NoAmount, uiautomationcore/ScrollAmount_SmallDecrement, uiautomationcore/ScrollAmount_SmallIncrement, winauto.uiauto_ScrollAmount
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScrollAmount
 - uiautomationcore/ScrollAmount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - ScrollAmount
---

# ScrollAmount enumeration


## -description

Contains values that specify the direction and distance to scroll.

## -enum-fields

### -field ScrollAmount_LargeDecrement:0

Scrolling is done in large decrements, equivalent to pressing the PAGE UP key or clicking on a blank part of a scroll bar. If one page up is not a relevant amount for the control and no scroll bar exists, the value represents an amount equal to the current visible window.

### -field ScrollAmount_SmallDecrement:1

Scrolling is done in small decrements, equivalent to pressing an arrow key or clicking the arrow button on a scroll bar.

### -field ScrollAmount_NoAmount:2

No scrolling is done.

### -field ScrollAmount_LargeIncrement:3

Scrolling is done in large increments, equivalent to pressing the PAGE DOWN or PAGE UP key or clicking on a blank part of a scroll bar. 
			If one page is not a relevant amount for the control and no scroll bar exists, the value represents an amount equal to the current visible window.

### -field ScrollAmount_SmallIncrement:4

Scrolling is done in small increments, equivalent to pressing an arrow key or clicking the arrow 
			button on a scroll bar.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iscrollprovider">IScrollProvider</a>
