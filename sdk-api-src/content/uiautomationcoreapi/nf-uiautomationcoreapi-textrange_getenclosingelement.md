---
UID: NF:uiautomationcoreapi.TextRange_GetEnclosingElement
title: TextRange_GetEnclosingElement function (uiautomationcoreapi.h)
description: Returns the node for the next smallest provider that covers the range.
helpviewer_keywords: ["TextRange_GetEnclosingElement","TextRange_GetEnclosingElement function [Windows Accessibility]","uiauto.uiauto_TextRange_GetEnclosingElementConPat","uiauto_TextRange_GetEnclosingElementConPat","uiautomationcoreapi/TextRange_GetEnclosingElement","winauto.uiauto_TextRange_GetEnclosingElementConPat"]
old-location: winauto\uiauto_TextRange_GetEnclosingElementConPat.htm
tech.root: WinAuto
ms.assetid: 842754a0-1fe7-4432-ab7f-716ef870df92
ms.date: 12/05/2018
ms.keywords: TextRange_GetEnclosingElement, TextRange_GetEnclosingElement function [Windows Accessibility], uiauto.uiauto_TextRange_GetEnclosingElementConPat, uiauto_TextRange_GetEnclosingElementConPat, uiautomationcoreapi/TextRange_GetEnclosingElement, winauto.uiauto_TextRange_GetEnclosingElementConPat
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
 - TextRange_GetEnclosingElement
 - uiautomationcoreapi/TextRange_GetEnclosingElement
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
 - TextRange_GetEnclosingElement
---

# TextRange_GetEnclosingElement function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Returns the node for the next smallest provider that covers the range.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param pRetVal [out]

Type: <b>HUIANODE*</b>

When this function returns, contains 
				the node for the next smallest element that encloses the range.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

The enclosing element is typically the text provider that supplies the text range. However,
		if the text provider supports child elements such as tables or hyperlinks, 
		the enclosing element could be a descendant of the text provider.