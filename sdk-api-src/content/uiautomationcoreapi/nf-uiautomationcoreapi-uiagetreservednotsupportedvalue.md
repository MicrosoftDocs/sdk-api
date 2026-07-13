---
UID: NF:uiautomationcoreapi.UiaGetReservedNotSupportedValue
title: UiaGetReservedNotSupportedValue function (uiautomationcoreapi.h)
description: Retrieves a reserved value indicating that a Microsoft UI Automation property or a text attribute is not supported.
helpviewer_keywords: ["UiaGetReservedNotSupportedValue","UiaGetReservedNotSupportedValue function [Windows Accessibility]","uiauto.uiauto_UiaGetReservedNotSupportedValueAutoMeth","uiauto_UiaGetReservedNotSupportedValueAutoMeth","uiautomationcoreapi/UiaGetReservedNotSupportedValue","winauto.uiauto_UiaGetReservedNotSupportedValueAutoMeth"]
old-location: winauto\uiauto_UiaGetReservedNotSupportedValueAutoMeth.htm
tech.root: WinAuto
ms.assetid: ba789ed0-fa34-492c-90b4-acee0adb634c
ms.date: 12/05/2018
ms.keywords: UiaGetReservedNotSupportedValue, UiaGetReservedNotSupportedValue function [Windows Accessibility], uiauto.uiauto_UiaGetReservedNotSupportedValueAutoMeth, uiauto_UiaGetReservedNotSupportedValueAutoMeth, uiautomationcoreapi/UiaGetReservedNotSupportedValue, winauto.uiauto_UiaGetReservedNotSupportedValueAutoMeth
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaGetReservedNotSupportedValue
 - uiautomationcoreapi/UiaGetReservedNotSupportedValue
dev_langs:
 - c++
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
---

# UiaGetReservedNotSupportedValue function


## -description

Retrieves a reserved value indicating that a Microsoft UI Automation property or a text attribute is not supported.

## -parameters

### -param punkNotSupportedValue [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives the object representing the value.
    This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-functions">Functions for Providers</a>



<a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>