---
UID: NF:uiautomationcoreapi.UiaRaiseAutomationPropertyChangedEvent
title: UiaRaiseAutomationPropertyChangedEvent function (uiautomationcoreapi.h)
author: windows-sdk-content
description: Called by providers to notify the Microsoft UI Automation core that an element property has changed.
old-location: winauto\uiauto_RaiseAutoPropChangedEventFunction.htm
tech.root: WinAuto
ms.assetid: ec9da198-eb1d-4883-9b5c-539c92bd530b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UiaRaiseAutomationPropertyChangedEvent, UiaRaiseAutomationPropertyChangedEvent function [Windows Accessibility], uiauto.uiauto_RaiseAutoPropChangedEventFunction, uiauto_RaiseAutoPropChangedEventFunction, uiautomationcoreapi/UiaRaiseAutomationPropertyChangedEvent, winauto.uiauto_RaiseAutoPropChangedEventFunction
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-uiacore-l1-1-0.dll
 - Ext-MS-Win-UIaCore-l1-1-1.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseAutomationPropertyChangedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaRaiseAutomationPropertyChangedEvent function


## -description


Called by providers to notify the Microsoft UI Automation core that an element property has changed.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider node where the property change event occurred.


### -param id [in]

Type: <b>PROPERTYID</b>

The identifier for the property that changed. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param oldValue [in]

Type: <b><a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a></b>

The old value of the property.


### -param newValue [in]

Type: <b><a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a></b>

The new value of the property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



