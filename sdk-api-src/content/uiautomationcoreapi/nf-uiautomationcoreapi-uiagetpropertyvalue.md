---
UID: NF:uiautomationcoreapi.UiaGetPropertyValue
title: UiaGetPropertyValue function (uiautomationcoreapi.h)
description: Retrieves the value of a UI Automation property.
helpviewer_keywords: ["UiaGetPropertyValue","UiaGetPropertyValue function [Windows Accessibility]","uiauto.uiauto_UiaGetPropertyValueAutoMeth","uiauto_UiaGetPropertyValueAutoMeth","uiautomationcoreapi/UiaGetPropertyValue","winauto.uiauto_UiaGetPropertyValueAutoMeth"]
old-location: winauto\uiauto_UiaGetPropertyValueAutoMeth.htm
tech.root: WinAuto
ms.assetid: 17d5450c-0894-412f-a8d1-44ea0364a606
ms.date: 12/05/2018
ms.keywords: UiaGetPropertyValue, UiaGetPropertyValue function [Windows Accessibility], uiauto.uiauto_UiaGetPropertyValueAutoMeth, uiauto_UiaGetPropertyValueAutoMeth, uiautomationcoreapi/UiaGetPropertyValue, winauto.uiauto_UiaGetPropertyValueAutoMeth
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - UiaGetPropertyValue
 - uiautomationcoreapi/UiaGetPropertyValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaGetPropertyValue
---

# UiaGetPropertyValue function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the value of a UI Automation property.

## -parameters

### -param hnode [in]

Type: <b>HUIANODE</b>

The element that the property is being requested from.

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param pValue [out]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

Receives the value of the specified property, or the value returned by <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue">UiaGetReservedNotSupportedValue</a> if the property is not supported.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.