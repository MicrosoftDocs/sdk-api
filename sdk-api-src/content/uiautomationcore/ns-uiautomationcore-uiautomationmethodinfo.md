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

# UIAutomationMethodInfo structure


## -description


Contains information about a method that is supported by a custom control pattern.


## -struct-fields




### -field pProgrammaticName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the method (a non-localizable string).


### -field doSetFocus

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if UI Automation should set the focus on the object before calling the method; otherwise <b>FALSE</b>.


### -field cInParameters

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The count of [in] parameters, which are always first in the <b>pParameterTypes</b> array.


### -field cOutParameters

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The count of [out] parameters, which always follow the [in] parameters in the <b>pParameterTypes</b> array.


### -field pParameterTypes

Type: <b><a href="https://msdn.microsoft.com/6090d5b5-2376-43ce-bef2-49bb3515107a">UIAutomationType</a>*</b>

A pointer to an array of values indicating the data types of the parameters of the method. The data types of the In parameters should be first, followed by those of the Out parameters.


### -field pParameterNames

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a>*</b>

A pointer to an array containing the parameter names (non-localizable strings).


## -see-also




<a href="https://msdn.microsoft.com/d1eca598-1a02-4437-8036-77c8d62032d5">Custom Properties, Events, and Control Patterns</a>



<a href="https://msdn.microsoft.com/f45c5736-75f3-4e44-b92a-3b0a51b41849">UIAutomationPatternInfo</a>
 

 

