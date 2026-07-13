---
UID: NF:uiautomationcoreapi.MultipleViewPattern_GetViewName
title: MultipleViewPattern_GetViewName function (uiautomationcoreapi.h)
description: Retrieves the name of a control-specific view. (MultipleViewPattern_GetViewName)
helpviewer_keywords: ["MultipleViewPattern_GetViewName","MultipleViewPattern_GetViewName function [Windows Accessibility]","uiauto.uiauto_MultipleViewPattern_GetViewNameConPat","uiauto_MultipleViewPattern_GetViewNameConPat","uiautomationcoreapi/MultipleViewPattern_GetViewName","winauto.uiauto_MultipleViewPattern_GetViewNameConPat"]
old-location: winauto\uiauto_MultipleViewPattern_GetViewNameConPat.htm
tech.root: WinAuto
ms.assetid: 950d9649-0565-4e1b-bdc7-49d1df7bbcd4
ms.date: 12/05/2018
ms.keywords: MultipleViewPattern_GetViewName, MultipleViewPattern_GetViewName function [Windows Accessibility], uiauto.uiauto_MultipleViewPattern_GetViewNameConPat, uiauto_MultipleViewPattern_GetViewNameConPat, uiautomationcoreapi/MultipleViewPattern_GetViewName, winauto.uiauto_MultipleViewPattern_GetViewNameConPat
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
 - MultipleViewPattern_GetViewName
 - uiautomationcoreapi/MultipleViewPattern_GetViewName
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
 - MultipleViewPattern_GetViewName
---

# MultipleViewPattern_GetViewName function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the name of a control-specific view.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The <i>control pattern</i> object.

### -param viewId [in]

Type: <b>int</b>

The integer identifier for the view.

### -param ppStr [out]

Type: <b>BSTR*</b>

When this function returns, contains a pointer to the string containing the name of the view. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.
