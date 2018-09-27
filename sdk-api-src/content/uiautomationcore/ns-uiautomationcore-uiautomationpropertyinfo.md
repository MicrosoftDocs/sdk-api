---
UID: NS:uiautomationcore.UIAutomationPropertyInfo
title: UIAutomationPropertyInfo
author: windows-sdk-content
description: Contains information about a custom property.
old-location: winauto\uiauto_UIAutomationPropertyInfoStruct.htm
tech.root: WinAuto
ms.assetid: ea5b4cbe-5a39-407c-9c61-8e9ac4f3398f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: UIAutomationPropertyInfo, UIAutomationPropertyInfo structure [Windows Accessibility], uiauto.uiauto_UIAutomationPropertyInfoStruct, uiauto_UIAutomationPropertyInfoStruct, uiautomationcore/UIAutomationPropertyInfo, winauto.uiauto_UIAutomationPropertyInfoStruct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - UIAutomationPropertyInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<li><a href="https://msdn.microsoft.com/en-us/library/Ee684080(v=VS.85).aspx">UIAutomationType_Bool</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/Ee684080(v=VS.85).aspx">UIAutomationType_Double</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/Ee684080(v=VS.85).aspx">UIAutomationType_Element</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/Ee684080(v=VS.85).aspx">UIAutomationType_Int</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/Ee684080(v=VS.85).aspx">UIAutomationType_Point</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/Ee684080(v=VS.85).aspx">UIAutomationType_String</a></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d1eca598-1a02-4437-8036-77c8d62032d5">Custom Properties, Events, and Control Patterns</a>



<a href="https://msdn.microsoft.com/225bbbec-5910-4711-b713-3409c9925be2">RegisterProperty</a>
 

 

