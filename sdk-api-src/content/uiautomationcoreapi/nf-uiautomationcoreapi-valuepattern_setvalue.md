---
UID: NF:uiautomationcoreapi.ValuePattern_SetValue
title: ValuePattern_SetValue function (uiautomationcoreapi.h)
description: Sets the text value of an element.
helpviewer_keywords: ["ValuePattern_SetValue","ValuePattern_SetValue function [Windows Accessibility]","uiauto.uiauto_ValuePattern_SetValueConPat","uiauto_ValuePattern_SetValueConPat","uiautomationcoreapi/ValuePattern_SetValue","winauto.uiauto_ValuePattern_SetValueConPat"]
old-location: winauto\uiauto_ValuePattern_SetValueConPat.htm
tech.root: WinAuto
ms.assetid: 6233abb0-7d18-4d1f-a611-28931d874bda
ms.date: 12/05/2018
ms.keywords: ValuePattern_SetValue, ValuePattern_SetValue function [Windows Accessibility], uiauto.uiauto_ValuePattern_SetValueConPat, uiauto_ValuePattern_SetValueConPat, uiautomationcoreapi/ValuePattern_SetValue, winauto.uiauto_ValuePattern_SetValueConPat
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
 - ValuePattern_SetValue
 - uiautomationcoreapi/ValuePattern_SetValue
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
 - ValuePattern_SetValue
---

# ValuePattern_SetValue function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sets the text value of an element.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

### -param pVal [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The string to set the element's content to.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.