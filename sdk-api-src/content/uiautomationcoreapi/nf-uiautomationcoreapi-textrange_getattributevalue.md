---
UID: NF:uiautomationcoreapi.TextRange_GetAttributeValue
title: TextRange_GetAttributeValue function (uiautomationcoreapi.h)
description: Gets the value of a text attribute for a text range.
helpviewer_keywords: ["TextRange_GetAttributeValue","TextRange_GetAttributeValue function [Windows Accessibility]","uiauto.uiauto_TextRange_GetAttributeValueConPat","uiauto_TextRange_GetAttributeValueConPat","uiautomationcoreapi/TextRange_GetAttributeValue","winauto.uiauto_TextRange_GetAttributeValueConPat"]
old-location: winauto\uiauto_TextRange_GetAttributeValueConPat.htm
tech.root: WinAuto
ms.assetid: f5d90dba-7c84-45a8-be84-898d6079c428
ms.date: 12/05/2018
ms.keywords: TextRange_GetAttributeValue, TextRange_GetAttributeValue function [Windows Accessibility], uiauto.uiauto_TextRange_GetAttributeValueConPat, uiauto_TextRange_GetAttributeValueConPat, uiautomationcoreapi/TextRange_GetAttributeValue, winauto.uiauto_TextRange_GetAttributeValueConPat
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
 - TextRange_GetAttributeValue
 - uiautomationcoreapi/TextRange_GetAttributeValue
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
 - TextRange_GetAttributeValue
---

# TextRange_GetAttributeValue function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the value of a text attribute for a text range.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param attributeId [in]

Type: <b>TEXTATTRIBUTEID</b>

The text attribute whose value is wanted. For a list of text attribute IDs, see <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a>.

### -param pRetVal [out]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

When this function returns, contains 
				the value of the attribute for the text range.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.