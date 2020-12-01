---
UID: NF:uiautomationcoreapi.TextPattern_GetSelection
title: TextPattern_GetSelection function (uiautomationcoreapi.h)
description: Gets the current range of selected text from a text container supporting the text pattern.
helpviewer_keywords: ["TextPattern_GetSelection","TextPattern_GetSelection function [Windows Accessibility]","uiauto.uiauto_TextPattern_GetSelectionConPat","uiauto_TextPattern_GetSelectionConPat","uiautomationcoreapi/TextPattern_GetSelection","winauto.uiauto_TextPattern_GetSelectionConPat"]
old-location: winauto\uiauto_TextPattern_GetSelectionConPat.htm
tech.root: WinAuto
ms.assetid: 277768af-ac6e-441c-8bf1-27a2c95a109c
ms.date: 12/05/2018
ms.keywords: TextPattern_GetSelection, TextPattern_GetSelection function [Windows Accessibility], uiauto.uiauto_TextPattern_GetSelectionConPat, uiauto_TextPattern_GetSelectionConPat, uiautomationcoreapi/TextPattern_GetSelection, winauto.uiauto_TextPattern_GetSelectionConPat
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
 - TextPattern_GetSelection
 - uiautomationcoreapi/TextPattern_GetSelection
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
 - TextPattern_GetSelection
---

# TextPattern_GetSelection function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the current range of selected text from a text container supporting the text pattern.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

A control pattern object.

### -param pRetVal [out]

Type: <b>HUIATEXTRANGE*</b>

When this function returns, contains 
				the text range spanning the currently selected text in the container. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.