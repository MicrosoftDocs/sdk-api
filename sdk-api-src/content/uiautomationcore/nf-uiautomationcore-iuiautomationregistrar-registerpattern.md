---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

