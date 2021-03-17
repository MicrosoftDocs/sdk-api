---
UID: NF:uiautomationcoreapi.TextRange_GetChildren
title: TextRange_GetChildren function (uiautomationcoreapi.h)
description: Returns all UI Automation elements contained within the specified text range.
helpviewer_keywords: ["TextRange_GetChildren","TextRange_GetChildren function [Windows Accessibility]","uiauto.uiauto_TextRange_GetChildrenConPat","uiauto_TextRange_GetChildrenConPat","uiautomationcoreapi/TextRange_GetChildren","winauto.uiauto_TextRange_GetChildrenConPat"]
old-location: winauto\uiauto_TextRange_GetChildrenConPat.htm
tech.root: WinAuto
ms.assetid: b8ee94c3-3da2-4f66-ba75-64bc4d40543b
ms.date: 12/05/2018
ms.keywords: TextRange_GetChildren, TextRange_GetChildren function [Windows Accessibility], uiauto.uiauto_TextRange_GetChildrenConPat, uiauto_TextRange_GetChildrenConPat, uiautomationcoreapi/TextRange_GetChildren, winauto.uiauto_TextRange_GetChildrenConPat
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
 - TextRange_GetChildren
 - uiautomationcoreapi/TextRange_GetChildren
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
 - TextRange_GetChildren
---

# TextRange_GetChildren function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Returns all UI Automation elements contained within the specified text range.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param pRetVal [out]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

When this function returns, contains 
				an array of nodes that are children of the text range in the UI Automation tree.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.