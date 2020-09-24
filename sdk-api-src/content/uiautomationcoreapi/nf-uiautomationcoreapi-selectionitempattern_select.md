---
UID: NF:uiautomationcoreapi.SelectionItemPattern_Select
title: SelectionItemPattern_Select function (uiautomationcoreapi.h)
description: Selects an element in a selection container.
helpviewer_keywords: ["SelectionItemPattern_Select","SelectionItemPattern_Select function [Windows Accessibility]","uiauto.uiauto_SelectionItemPattern_SelectConPat","uiauto_SelectionItemPattern_SelectConPat","uiautomationcoreapi/SelectionItemPattern_Select","winauto.uiauto_SelectionItemPattern_SelectConPat"]
old-location: winauto\uiauto_SelectionItemPattern_SelectConPat.htm
tech.root: WinAuto
ms.assetid: 73cc27bd-b309-4de1-9249-23b0b209db3c
ms.date: 12/05/2018
ms.keywords: SelectionItemPattern_Select, SelectionItemPattern_Select function [Windows Accessibility], uiauto.uiauto_SelectionItemPattern_SelectConPat, uiauto_SelectionItemPattern_SelectConPat, uiautomationcoreapi/SelectionItemPattern_Select, winauto.uiauto_SelectionItemPattern_SelectConPat
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
 - SelectionItemPattern_Select
 - uiautomationcoreapi/SelectionItemPattern_Select
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
 - SelectionItemPattern_Select
---

# SelectionItemPattern_Select function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Selects an element in a selection container.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

All other elements are deselected. 
To select an element without deselecting others, use <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-selectionitempattern_addtoselection">SelectionItemPattern_AddToSelection</a>.