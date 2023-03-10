---
UID: NF:uiautomationcoreapi.SelectionItemPattern_AddToSelection
title: SelectionItemPattern_AddToSelection function (uiautomationcoreapi.h)
description: Adds an unselected element to a selection in a control.
helpviewer_keywords: ["SelectionItemPattern_AddToSelection","SelectionItemPattern_AddToSelection function [Windows Accessibility]","uiauto.uiauto_SelectionItemPattern_AddToSelectionConPat","uiauto_SelectionItemPattern_AddToSelectionConPat","uiautomationcoreapi/SelectionItemPattern_AddToSelection","winauto.uiauto_SelectionItemPattern_AddToSelectionConPat"]
old-location: winauto\uiauto_SelectionItemPattern_AddToSelectionConPat.htm
tech.root: WinAuto
ms.assetid: 77ded493-cdf5-4e1b-b0eb-640ec46cf43a
ms.date: 12/05/2018
ms.keywords: SelectionItemPattern_AddToSelection, SelectionItemPattern_AddToSelection function [Windows Accessibility], uiauto.uiauto_SelectionItemPattern_AddToSelectionConPat, uiauto_SelectionItemPattern_AddToSelectionConPat, uiautomationcoreapi/SelectionItemPattern_AddToSelection, winauto.uiauto_SelectionItemPattern_AddToSelectionConPat
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
 - SelectionItemPattern_AddToSelection
 - uiautomationcoreapi/SelectionItemPattern_AddToSelection
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
 - SelectionItemPattern_AddToSelection
---

# SelectionItemPattern_AddToSelection function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Adds an unselected element to a selection in a control.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

In a control that supports multiple selection, this function adds an item to the selection. In a single-selection control,
it deselects the currently selected item and selects the specified item.