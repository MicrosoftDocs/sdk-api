---
UID: NF:uiautomationcore.IUIAutomationRegistrar.RegisterPattern
title: IUIAutomationRegistrar::RegisterPattern
author: windows-sdk-content
description: Registers a third-party control pattern.
old-location: winauto\uiauto_IUIAutomationRegistrar_RegisterPattern.htm
old-project: WinAuto
ms.assetid: 6aa61295-e035-4a51-9157-7cf9cfaee37a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IUIAutomationRegistrar interface [Windows Accessibility],RegisterPattern method, IUIAutomationRegistrar.RegisterPattern, IUIAutomationRegistrar::RegisterPattern, RegisterPattern, RegisterPattern method [Windows Accessibility], RegisterPattern method [Windows Accessibility],IUIAutomationRegistrar interface, uiauto.uiauto_IUIAutomationRegistrar_RegisterPattern, uiauto_IUIAutomationRegistrar_RegisterPattern, uiautomationcore/IUIAutomationRegistrar::RegisterPattern, winauto.uiauto_IUIAutomationRegistrar_RegisterPattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IUIAutomationRegistrar.RegisterPattern
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationRegistrar::RegisterPattern


## -description


Registers a third-party control pattern.


## -parameters




### -param pattern [in]

Type: <b><a href="https://msdn.microsoft.com/f45c5736-75f3-4e44-b92a-3b0a51b41849">UIAutomationPatternInfo</a>*</b>

A pointer to a structure that contains information about the control pattern to register.


### -param pPatternId




### -param pPatternAvailablePropertyId [out]

Type: <b>PROPERTYID*</b>

Receives the property identifier for the pattern.  This value can be used with UI Automation client methods to determine whether the element supports the new pattern. This is equivalent to values such as <a href="uiauto_control_pattern_availability_propids.htm">UIA_IsInvokePatternAvailablePropertyId</a>.


### -param propertyIdCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of properties supported by the control pattern.


### -param pPropertyIds [out]

Type: <b>PROPERTYID*</b>

Receives an array of identifiers for properties supported by the pattern.


### -param eventIdCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of events supported by the control pattern. 


### -param pEventIds [out]

Type: <b>EVENTID*</b>

Receives an array of identifiers for events that are raised by the pattern.


#### - patternId [out]

Type: <b>PATTERNID*</b>

Receives the pattern identifier.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The pattern, property, and event IDs retrieved by this method can be used in <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> implementations.




## -see-also




<a href="https://msdn.microsoft.com/b5d979aa-7a87-4d6c-acdc-6e9eb19aac98">IUIAutomationRegistrar</a>
 

 

