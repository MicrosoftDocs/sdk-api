---
UID: NF:uiautomationcore.IScrollProvider.get_HorizontallyScrollable
title: IScrollProvider::get_HorizontallyScrollable
author: windows-sdk-content
description: Indicates whether the control can scroll horizontally.
old-location: winauto\uiauto_IScrollProvider_HorizontallyScrollable.htm
tech.root: WinAuto
ms.assetid: f9d073c0-b51a-4e62-ab67-872538a6a0e1
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: HorizontallyScrollable property [Windows Accessibility], HorizontallyScrollable property [Windows Accessibility],IScrollProvider interface, IScrollProvider interface [Windows Accessibility],HorizontallyScrollable property, IScrollProvider.HorizontallyScrollable, IScrollProvider.get_HorizontallyScrollable, IScrollProvider::HorizontallyScrollable, IScrollProvider::get_HorizontallyScrollable, get_HorizontallyScrollable, uiauto.uiauto_IScrollProvider_HorizontallyScrollable, uiauto_IScrollProvider_HorizontallyScrollable, uiautomationcore/IScrollProvider::HorizontallyScrollable, uiautomationcore/IScrollProvider::get_HorizontallyScrollable, winauto.uiauto_IScrollProvider_HorizontallyScrollable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IScrollProvider.HorizontallyScrollable
 - IScrollProvider.get_HorizontallyScrollable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IScrollProvider::get_HorizontallyScrollable


## -description


Indicates whether the control can scroll horizontally.
        

This property is read-only.


## -parameters


## -remarks



This property can be dynamic. For example, the content area of the control 
        might not be larger than the current viewable area, meaning <b>IScrollProvider::HorizontallyScrollable</b> 
        is <b>FALSE</b>. However, either resizing the control or adding child items may increase the bounds of the 
        content area beyond the viewable area, meaning <b>IScrollProvider::HorizontallyScrollable</b> is <b>TRUE</b>. 
        




## -see-also




<a href="https://msdn.microsoft.com/55e1b899-aa9f-45eb-9cfa-d645ea659988">IScrollProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

