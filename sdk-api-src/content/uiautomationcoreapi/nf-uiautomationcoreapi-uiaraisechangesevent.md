---
UID: NF:uiautomationcoreapi.UiaRaiseChangesEvent
title: UiaRaiseChangesEvent function
author: windows-sdk-content
description: Called by providers to notify the Microsoft UI Automation core that a change has occurred.
old-location: winauto\uiauto_UiaRaiseChangesEventFunction.htm
tech.root: WinAuto
ms.assetid: AA6F1F6E-3EE9-44A6-B1AE-B08013DC1E37
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: UiaRaiseChangesEvent, UiaRaiseChangesEvent function [Windows Accessibility], uiautomationcoreapi/UiaRaiseChangesEvent, winauto.uiauto_UiaRaiseChangesEventFunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseChangesEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaRaiseChangesEvent function


## -description


Called by providers to notify the Microsoft UI Automation core that a change has occurred.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider node where the change event occurred.


### -param eventIdCount [in]

The number of changes that occurred. This is the number of <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures pointed to by the <i>pUiaChanges</i> parameter.


### -param pUiaChanges [in]

A collection of pointers to <a href="https://msdn.microsoft.com/28C0C0DE-7ED2-4D01-B532-E56AD81AE8D0">UiaChangeInfo</a> structures.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> value indicating success or failure.



