---
UID: NS:uiautomationcore.UIAutomationMethodInfo
title: UIAutomationMethodInfo
author: windows-sdk-content
description: Contains information about a method that is supported by a custom control pattern.
old-location: winauto\uiauto_UIAutomationMethodInfoStruct.htm
tech.root: WinAuto
ms.assetid: 33a52126-8757-44d0-91e1-758f51e3d0f8
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: UIAutomationMethodInfo, UIAutomationMethodInfo structure [Windows Accessibility], uiauto.uiauto_UIAutomationMethodInfoStruct, uiauto_UIAutomationMethodInfoStruct, uiautomationcore/UIAutomationMethodInfo, winauto.uiauto_UIAutomationMethodInfoStruct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - UIAutomationMethodInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

