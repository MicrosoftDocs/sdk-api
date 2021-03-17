---
UID: NF:uiautomationcoreapi.TextPattern_GetVisibleRanges
title: TextPattern_GetVisibleRanges function (uiautomationcoreapi.h)
description: Retrieves an array of disjoint text ranges from a text container where each text range begins with the first partially visible line through to the end of the last partially visible line.
helpviewer_keywords: ["TextPattern_GetVisibleRanges","TextPattern_GetVisibleRanges function [Windows Accessibility]","uiauto.uiauto_TextPattern_GetVisibleRangesConPat","uiauto_TextPattern_GetVisibleRangesConPat","uiautomationcoreapi/TextPattern_GetVisibleRanges","winauto.uiauto_TextPattern_GetVisibleRangesConPat"]
old-location: winauto\uiauto_TextPattern_GetVisibleRangesConPat.htm
tech.root: WinAuto
ms.assetid: 509c1d6e-c7ae-4c74-8635-27071ea37696
ms.date: 12/05/2018
ms.keywords: TextPattern_GetVisibleRanges, TextPattern_GetVisibleRanges function [Windows Accessibility], uiauto.uiauto_TextPattern_GetVisibleRangesConPat, uiauto_TextPattern_GetVisibleRangesConPat, uiautomationcoreapi/TextPattern_GetVisibleRanges, winauto.uiauto_TextPattern_GetVisibleRangesConPat
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
 - TextPattern_GetVisibleRanges
 - uiautomationcoreapi/TextPattern_GetVisibleRanges
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
 - TextPattern_GetVisibleRanges
---

# TextPattern_GetVisibleRanges function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves an array of disjoint text ranges from a text container where each 
        text range begins with the first partially visible line through to the end of the 
        last partially visible line. For example, a multi-column layout where the columns 
        are partially scrolled out of the visible area of the viewport and the content 
        flows from the bottom of one column to the top of the next.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

A control pattern object.

### -param pRetVal [out]

Type: <b>HUIATEXTRANGE*</b>

When this function returns, contains
				an array of text ranges spanning the visible text within the text container. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.