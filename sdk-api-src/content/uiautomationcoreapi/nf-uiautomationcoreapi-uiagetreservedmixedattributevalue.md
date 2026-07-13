---
UID: NF:uiautomationcoreapi.UiaGetReservedMixedAttributeValue
title: UiaGetReservedMixedAttributeValue function (uiautomationcoreapi.h)
description: Retrieves a reserved value indicating that the value of a Microsoft UI Automation text attribute varies within a text range.
helpviewer_keywords: ["UiaGetReservedMixedAttributeValue","UiaGetReservedMixedAttributeValue function [Windows Accessibility]","uiauto.uiauto_UiaGetReservedMixedAttributeValueAutoMeth","uiauto_UiaGetReservedMixedAttributeValueAutoMeth","uiautomationcoreapi/UiaGetReservedMixedAttributeValue","winauto.uiauto_UiaGetReservedMixedAttributeValueAutoMeth"]
old-location: winauto\uiauto_UiaGetReservedMixedAttributeValueAutoMeth.htm
tech.root: WinAuto
ms.assetid: 597ace91-197a-4cda-9386-78c6e429871b
ms.date: 12/05/2018
ms.keywords: UiaGetReservedMixedAttributeValue, UiaGetReservedMixedAttributeValue function [Windows Accessibility], uiauto.uiauto_UiaGetReservedMixedAttributeValueAutoMeth, uiauto_UiaGetReservedMixedAttributeValueAutoMeth, uiautomationcoreapi/UiaGetReservedMixedAttributeValue, winauto.uiauto_UiaGetReservedMixedAttributeValueAutoMeth
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
 - UiaGetReservedMixedAttributeValue
 - uiautomationcoreapi/UiaGetReservedMixedAttributeValue
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
 - UiaGetReservedMixedAttributeValue
---

# UiaGetReservedMixedAttributeValue function


## -description

Retrieves a reserved value indicating that the value of a Microsoft UI Automation text attribute varies  within a text range.

## -parameters

### -param punkMixedAttributeValue [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives 
    a reserved value specifying that 
    an attribute varies over a text range.
    This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-functions">Functions for Providers</a>



<a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>