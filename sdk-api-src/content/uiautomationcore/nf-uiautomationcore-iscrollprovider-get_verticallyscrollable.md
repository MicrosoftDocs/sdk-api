---
UID: NF:uiautomationcore.IScrollProvider.get_VerticallyScrollable
title: IScrollProvider::get_VerticallyScrollable method
author: windows-driver-content
description: Indicates whether the control can scroll vertically.
old-location: winauto\uiauto_IScrollProvider_VerticallyScrollable.htm
old-project: WinAuto
ms.assetid: fadc0fd7-969c-4189-b37c-9b8243e30ac1
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IScrollProvider, IScrollProvider interface [Windows Accessibility], VerticallyScrollable property, IScrollProvider.VerticallyScrollable, IScrollProvider::get_VerticallyScrollable, VerticallyScrollable property [Windows Accessibility], VerticallyScrollable property [Windows Accessibility], IScrollProvider interface, get_VerticallyScrollable,IScrollProvider.get_VerticallyScrollable, uiauto.uiauto_IScrollProvider_VerticallyScrollable, uiauto_IScrollProvider_VerticallyScrollable, uiautomationcore/IScrollProvider::VerticallyScrollable, uiautomationcore/IScrollProvider::get_VerticallyScrollable, winauto.uiauto_IScrollProvider_VerticallyScrollable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.h
api_name:
-	IScrollProvider.VerticallyScrollable
-	IScrollProvider.get_VerticallyScrollable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScrollProvider::get_VerticallyScrollable method


## -description



        Indicates whether the control can scroll vertically.
        

This property is read-only.


## -parameters


## -remarks




        This property can be dynamic. For example, the content area of the control 
        might not be larger than the viewable area, meaning <b>IScrollProvider::VerticallyScrollable</b> 
        is <b>FALSE</b>. However, resizing the control or adding child items may increase the bounds of the 
        content area beyond the viewable area, meaning that <b>IScrollProvider::VerticallyScrollable</b> is <b>TRUE</b>. 
        




## -see-also




<a href="https://msdn.microsoft.com/55e1b899-aa9f-45eb-9cfa-d645ea659988">IScrollProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

