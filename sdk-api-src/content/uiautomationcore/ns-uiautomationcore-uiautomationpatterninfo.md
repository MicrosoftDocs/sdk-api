---
UID: NS:uiautomationcore.UIAutomationPatternInfo
title: UIAutomationPatternInfo
author: windows-sdk-content
description: Contains information about a custom control pattern.
old-location: winauto\uiauto_UIAutomationPatternInfoStruct.htm
tech.root: WinAuto
ms.assetid: f45c5736-75f3-4e44-b92a-3b0a51b41849
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UIAutomationPatternInfo, UIAutomationPatternInfo structure [Windows Accessibility], uiauto.uiauto_UIAutomationPatternInfoStruct, uiauto_UIAutomationPatternInfoStruct, uiautomationcore/UIAutomationPatternInfo, winauto.uiauto_UIAutomationPatternInfoStruct
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
 - UIAutomationPatternInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UIAutomationPatternInfo structure


## -description


Contains information about a custom control pattern.


## -struct-fields




### -field guid

Type: <b>GUID</b>

The unique identifier of the control pattern.


### -field pProgrammaticName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the control pattern (a non-localizable string).


### -field providerInterfaceId

Type: <b>GUID</b>

The unique identifier of the provider interface for the control pattern.


### -field clientInterfaceId

Type: <b>GUID</b>

The unique identifier of the client interface for the control pattern.


### -field cProperties

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The count of elements in <b>pProperties</b>.


### -field pProperties

Type: <b><a href="https://msdn.microsoft.com/ea5b4cbe-5a39-407c-9c61-8e9ac4f3398f">UIAutomationPropertyInfo</a>*</b>

A pointer to an array of structures describing properties available on the control pattern.


### -field cMethods

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The count of elements in <b>pMethods</b>.


### -field pMethods

Type: <b><a href="https://msdn.microsoft.com/33a52126-8757-44d0-91e1-758f51e3d0f8">UIAutomationMethodInfo</a>*</b>

A pointer to an array of structures describing methods available on the control pattern.


### -field cEvents

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The count of elements in <b>pEvents</b>.


### -field pEvents

Type: <b><a href="https://msdn.microsoft.com/05dd033f-3bb2-4185-9cfc-c19927a82406">UIAutomationEventInfo</a>*</b>

A pointer to an array of structures describing events available on the control pattern.


### -field pPatternHandler

Type: <b><a href="https://msdn.microsoft.com/6d0edd8e-3fd4-47d6-ab53-582eb81f38bd">IUIAutomationPatternHandler</a>*</b>

A pointer to the object that makes the control pattern available to clients.


## -see-also




<a href="https://msdn.microsoft.com/d1eca598-1a02-4437-8036-77c8d62032d5">Custom Properties, Events, and Control Patterns</a>



<a href="https://msdn.microsoft.com/6aa61295-e035-4a51-9157-7cf9cfaee37a">RegisterPattern</a>
 

 

