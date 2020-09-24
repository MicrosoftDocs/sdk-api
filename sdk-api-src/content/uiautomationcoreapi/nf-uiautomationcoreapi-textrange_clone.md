---
UID: NF:uiautomationcoreapi.TextRange_Clone
title: TextRange_Clone function (uiautomationcoreapi.h)
description: Copies a text range.
helpviewer_keywords: ["TextRange_Clone","TextRange_Clone function [Windows Accessibility]","uiauto.uiauto_TextRange_CloneConPat","uiauto_TextRange_CloneConPat","uiautomationcoreapi/TextRange_Clone","winauto.uiauto_TextRange_CloneConPat"]
old-location: winauto\uiauto_TextRange_CloneConPat.htm
tech.root: WinAuto
ms.assetid: df067f6b-f15f-48cf-979a-d1a9bfbdc05f
ms.date: 12/05/2018
ms.keywords: TextRange_Clone, TextRange_Clone function [Windows Accessibility], uiauto.uiauto_TextRange_CloneConPat, uiauto_TextRange_CloneConPat, uiautomationcoreapi/TextRange_Clone, winauto.uiauto_TextRange_CloneConPat
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
 - TextRange_Clone
 - uiautomationcoreapi/TextRange_Clone
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
 - TextRange_Clone
---

# TextRange_Clone function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Copies a text range.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param pRetVal [out]

Type: <b>HUIATEXTRANGE*</b>

When this function returns, contains the copy. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

The method never returns <b>NULL</b> (Nothing in Microsoft Visual Basic .NET).

The new range can be manipulated independently from the original.