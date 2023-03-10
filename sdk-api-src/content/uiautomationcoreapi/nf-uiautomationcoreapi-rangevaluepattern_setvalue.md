---
UID: NF:uiautomationcoreapi.RangeValuePattern_SetValue
title: RangeValuePattern_SetValue function (uiautomationcoreapi.h)
description: Sets the value of a control that has a numerical range.
helpviewer_keywords: ["RangeValuePattern_SetValue","RangeValuePattern_SetValue function [Windows Accessibility]","uiauto.uiauto_RangeValuePattern_SetValueConPat","uiauto_RangeValuePattern_SetValueConPat","uiautomationcoreapi/RangeValuePattern_SetValue","winauto.uiauto_RangeValuePattern_SetValueConPat"]
old-location: winauto\uiauto_RangeValuePattern_SetValueConPat.htm
tech.root: WinAuto
ms.assetid: 9a001826-fb0f-4e68-ba0f-54736d6ca1bd
ms.date: 12/05/2018
ms.keywords: RangeValuePattern_SetValue, RangeValuePattern_SetValue function [Windows Accessibility], uiauto.uiauto_RangeValuePattern_SetValueConPat, uiauto_RangeValuePattern_SetValueConPat, uiautomationcoreapi/RangeValuePattern_SetValue, winauto.uiauto_RangeValuePattern_SetValueConPat
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
 - RangeValuePattern_SetValue
 - uiautomationcoreapi/RangeValuePattern_SetValue
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
 - RangeValuePattern_SetValue
---

# RangeValuePattern_SetValue function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sets the value of a control that has a numerical range.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

### -param val [in]

Type: <b>double</b>

The value to set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.