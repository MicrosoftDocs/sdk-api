---
UID: NF:uiautomationcoreapi.GridPattern_GetItem
title: GridPattern_GetItem function (uiautomationcoreapi.h)
description: Gets the node for an item in a grid.
helpviewer_keywords: ["GridPattern_GetItem","GridPattern_GetItem function [Windows Accessibility]","uiauto.uiauto_GridPattern_GetItemConPat","uiauto_GridPattern_GetItemConPat","uiautomationcoreapi/GridPattern_GetItem","winauto.uiauto_GridPattern_GetItemConPat"]
old-location: winauto\uiauto_GridPattern_GetItemConPat.htm
tech.root: WinAuto
ms.assetid: 776b704b-479b-4b01-8522-b50500bf1c84
ms.date: 12/05/2018
ms.keywords: GridPattern_GetItem, GridPattern_GetItem function [Windows Accessibility], uiauto.uiauto_GridPattern_GetItemConPat, uiauto_GridPattern_GetItemConPat, uiautomationcoreapi/GridPattern_GetItem, winauto.uiauto_GridPattern_GetItemConPat
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
 - GridPattern_GetItem
 - uiautomationcoreapi/GridPattern_GetItem
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
 - GridPattern_GetItem
---

# GridPattern_GetItem function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the node for an item in a grid.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.

### -param row [in]

Type: <b>int</b>

The row of the node being requested.

### -param column [in]

Type: <b>int</b>

The column of the node being requested.

### -param pResult [out]

Type: <b>HUIANODE*</b>

When this function returns, contains a pointer to the node for the cell 
				at the specified location. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

Row 0, column 0 is the first item in a grid.