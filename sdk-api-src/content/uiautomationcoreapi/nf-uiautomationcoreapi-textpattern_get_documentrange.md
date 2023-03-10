---
UID: NF:uiautomationcoreapi.TextPattern_get_DocumentRange
title: TextPattern_get_DocumentRange function (uiautomationcoreapi.h)
description: Gets the text range for the entire document.
helpviewer_keywords: ["TextPattern_get_DocumentRange","TextPattern_get_DocumentRange function [Windows Accessibility]","uiauto.uiauto_TextPattern_get_DocumentRangeConPat","uiauto_TextPattern_get_DocumentRangeConPat","uiautomationcoreapi/TextPattern_get_DocumentRange","winauto.uiauto_TextPattern_get_DocumentRangeConPat"]
old-location: winauto\uiauto_TextPattern_get_DocumentRangeConPat.htm
tech.root: WinAuto
ms.assetid: e1ef5608-166c-4ab7-9f8d-ed8a4afd3b5a
ms.date: 12/05/2018
ms.keywords: TextPattern_get_DocumentRange, TextPattern_get_DocumentRange function [Windows Accessibility], uiauto.uiauto_TextPattern_get_DocumentRangeConPat, uiauto_TextPattern_get_DocumentRangeConPat, uiautomationcoreapi/TextPattern_get_DocumentRange, winauto.uiauto_TextPattern_get_DocumentRangeConPat
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
 - TextPattern_get_DocumentRange
 - uiautomationcoreapi/TextPattern_get_DocumentRange
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
 - TextPattern_get_DocumentRange
---

# TextPattern_get_DocumentRange function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the text range for the entire document.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

A control pattern object.

### -param pRetVal [out]

Type: <b>HUIATEXTRANGE*</b>

When this function returns, contains 
				the text range spanning the entire document contents of the text container. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.