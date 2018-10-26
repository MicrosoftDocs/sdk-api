---
UID: NF:uiautomationclient.IUIAutomationElement.get_CachedControlType
title: IUIAutomationElement::get_CachedControlType
author: windows-sdk-content
description: Retrieves a cached value that indicates the control type of the element.
old-location: winauto\uiauto_IUIAutomationElement_CachedControlType.htm
tech.root: WinAuto
ms.assetid: 48b232a8-8826-4c70-b541-3e6a792105c1
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CachedControlType property [Windows Accessibility], CachedControlType property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CachedControlType property, IUIAutomationElement.CachedControlType, IUIAutomationElement.get_CachedControlType, IUIAutomationElement::CachedControlType, IUIAutomationElement::get_CachedControlType, get_CachedControlType, uiauto.uiauto_IUIAutomationElement_CachedControlType, uiauto_IUIAutomationElement_CachedControlType, uiautomationclient/IUIAutomationElement::CachedControlType, uiautomationclient/IUIAutomationElement::get_CachedControlType, winauto.uiauto_IUIAutomationElement_CachedControlType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - UIAutomationClient.h
api_name:
 - IUIAutomationElement.CachedControlType
 - IUIAutomationElement.get_CachedControlType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement::get_CachedControlType


## -description


Retrieves a cached value that indicates the control type of the element.

This property is read-only.


## -parameters


## -remarks



Control types describe a known interaction model for UI Automation elements without relying on a localized control type or combination of complex logic rules. This property cannot change at run time unless the control supports the <a href="https://msdn.microsoft.com/4a1613b9-1e64-4d4e-876e-e2bf886097d4">IUIAutomationMultipleViewPattern</a> interface. An example is the Win32 ListView control, which can change from a data grid to a list, depending on the current view.




## -see-also




<a href="https://msdn.microsoft.com/f7613ad1-0b75-46fb-b9ac-b1ae9eea4193">Automation Element Property IDs</a>



<a href="https://msdn.microsoft.com/6bceeabd-be77-4820-842a-d343fa2857bd">CurrentControlType</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>
 

 

