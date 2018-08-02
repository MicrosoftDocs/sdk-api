---
UID: NF:uiautomationcoreapi.UiaGetReservedMixedAttributeValue
title: UiaGetReservedMixedAttributeValue function
author: windows-sdk-content
description: Retrieves a reserved value indicating that the value of a Microsoft UI Automation text attribute varies within a text range.
old-location: winauto\uiauto_UiaGetReservedMixedAttributeValueAutoMeth.htm
old-project: WinAuto
ms.assetid: 597ace91-197a-4cda-9386-78c6e429871b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: UiaGetReservedMixedAttributeValue, UiaGetReservedMixedAttributeValue function [Windows Accessibility], uiauto.uiauto_UiaGetReservedMixedAttributeValueAutoMeth, uiauto_UiaGetReservedMixedAttributeValueAutoMeth, uiautomationcoreapi/UiaGetReservedMixedAttributeValue, winauto.uiauto_UiaGetReservedMixedAttributeValueAutoMeth
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
 - UiaGetReservedMixedAttributeValue
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaGetReservedMixedAttributeValue function


## -description


Retrieves a reserved value indicating that the value of a Microsoft UI Automation text attribute varies  within a text range.


## -parameters




### -param punkMixedAttributeValue [out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives 
    a reserved value specifying that 
    an attribute varies over a text range.
    This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/76012ec7-0114-4b6b-a35e-5cfde5b90230">Functions for Providers</a>



<a href="https://msdn.microsoft.com/4d541c31-11f7-4d7e-a0e0-9ed1da873d07">Text and TextRange Control Patterns</a>
 

 

