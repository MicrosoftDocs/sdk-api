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

# UIAutomationPropertyInfo structure


## -description


Contains information about a custom property.


## -struct-fields




### -field guid

Type: <b>GUID</b>

The unique identifier of the property.


### -field pProgrammaticName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The programmatic name of the property (a non-localizable string).


### -field type

Type: <b><a href="https://msdn.microsoft.com/6090d5b5-2376-43ce-bef2-49bb3515107a">UIAutomationType</a></b>

A value from the <a href="https://msdn.microsoft.com/6090d5b5-2376-43ce-bef2-49bb3515107a">UIAutomationType</a> enumerated type indicating the data type of the property value.


## -remarks



A custom property must have one of the following data types specified by the <a href="https://msdn.microsoft.com/6090d5b5-2376-43ce-bef2-49bb3515107a">UIAutomationType</a> enumeration. No other data types are supported for custom properties. For more information, see <a href="https://msdn.microsoft.com/d1eca598-1a02-4437-8036-77c8d62032d5">Custom Properties, Events, and Control Patterns</a>.


<ul>
<li><a href="uiauto_UIAutomationTypeEnum.htm">UIAutomationType_Bool</a></li>
<li><a href="uiauto_UIAutomationTypeEnum.htm">UIAutomationType_Double</a></li>
<li><a href="uiauto_UIAutomationTypeEnum.htm">UIAutomationType_Element</a></li>
<li><a href="uiauto_UIAutomationTypeEnum.htm">UIAutomationType_Int</a></li>
<li><a href="uiauto_UIAutomationTypeEnum.htm">UIAutomationType_Point</a></li>
<li><a href="uiauto_UIAutomationTypeEnum.htm">UIAutomationType_String</a></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d1eca598-1a02-4437-8036-77c8d62032d5">Custom Properties, Events, and Control Patterns</a>



<a href="https://msdn.microsoft.com/225bbbec-5910-4711-b713-3409c9925be2">RegisterProperty</a>
 

 

