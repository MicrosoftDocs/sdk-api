---
UID: NF:uiautomationcore.IValueProvider.get_IsReadOnly
title: IValueProvider::get_IsReadOnly
author: windows-sdk-content
description: Indicates whether the value of a control is read-only.
old-location: winauto\uiauto_IValueProvider_IsReadOnly.htm
tech.root: WinAuto
ms.assetid: 2dadeb17-aef8-4dcd-a2c5-251cc2e7de3f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IValueProvider interface [Windows Accessibility],IsReadOnly property, IValueProvider.IsReadOnly, IValueProvider.get_IsReadOnly, IValueProvider::IsReadOnly, IValueProvider::get_IsReadOnly, IsReadOnly property [Windows Accessibility], IsReadOnly property [Windows Accessibility],IValueProvider interface, get_IsReadOnly, uiauto.uiauto_IValueProvider_IsReadOnly, uiauto_IValueProvider_IsReadOnly, uiautomationcore/IValueProvider::IsReadOnly, uiautomationcore/IValueProvider::get_IsReadOnly, winauto.uiauto_IValueProvider_IsReadOnly
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
 - IValueProvider.IsReadOnly
 - IValueProvider.get_IsReadOnly
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IValueProvider::get_IsReadOnly


## -description


Indicates whether the value of a control is read-only. 

This property is read-only.


## -parameters


## -remarks



A control should have its IsEnabled property (<a href="uiauto_automation_element_propids.htm">UIA_IsEnabledPropertyId</a>) set to <b>TRUE</b> and its <b>IValueProvider::IsReadOnly</b> 
            property set to <b>FALSE</b> before allowing a call to <a href="https://msdn.microsoft.com/af555ac6-5abd-4019-804b-68f9ed3be801">IValueProvider::SetValue</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/e6adbc23-dbfe-4dd2-82d9-66ce16de3338">IValueProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

