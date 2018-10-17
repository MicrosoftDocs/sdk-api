---
UID: NF:uiautomationcoreapi.UiaGetReservedNotSupportedValue
title: UiaGetReservedNotSupportedValue function
author: windows-sdk-content
description: Retrieves a reserved value indicating that a Microsoft UI Automation property or a text attribute is not supported.
old-location: winauto\uiauto_UiaGetReservedNotSupportedValueAutoMeth.htm
tech.root: WinAuto
ms.assetid: ba789ed0-fa34-492c-90b4-acee0adb634c
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: UiaGetReservedNotSupportedValue, UiaGetReservedNotSupportedValue function [Windows Accessibility], uiauto.uiauto_UiaGetReservedNotSupportedValueAutoMeth, uiauto_UiaGetReservedNotSupportedValueAutoMeth, uiautomationcoreapi/UiaGetReservedNotSupportedValue, winauto.uiauto_UiaGetReservedNotSupportedValueAutoMeth
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - UiaGetReservedNotSupportedValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaGetReservedNotSupportedValue function


## -description


Retrieves a reserved value indicating that a Microsoft UI Automation property or a text attribute is not supported.


## -parameters




### -param punkNotSupportedValue [out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives the object representing the value.
    This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/76012ec7-0114-4b6b-a35e-5cfde5b90230">Functions for Providers</a>



<a href="https://msdn.microsoft.com/4d541c31-11f7-4d7e-a0e0-9ed1da873d07">Text and TextRange Control Patterns</a>
 

 

