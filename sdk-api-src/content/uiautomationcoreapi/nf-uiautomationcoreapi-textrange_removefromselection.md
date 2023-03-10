---
UID: NF:uiautomationcoreapi.TextRange_RemoveFromSelection
title: TextRange_RemoveFromSelection function (uiautomationcoreapi.h)
description: Removes the selected text, corresponding to the calling text range TextPatternRangeEndpoint_Start and TextPatternRangeEndpoint_End endpoints, from an existing collection of selected text in a text container that supports multiple, disjoint selections.
helpviewer_keywords: ["TextRange_RemoveFromSelection","TextRange_RemoveFromSelection function [Windows Accessibility]","uiauto.uiauto_TextRange_RemoveFromSelectionConPat","uiauto_TextRange_RemoveFromSelectionConPat","uiautomationcoreapi/TextRange_RemoveFromSelection","winauto.uiauto_TextRange_RemoveFromSelectionConPat"]
old-location: winauto\uiauto_TextRange_RemoveFromSelectionConPat.htm
tech.root: WinAuto
ms.assetid: c8de1889-82e8-4147-9c71-f77bf05c72a0
ms.date: 12/05/2018
ms.keywords: TextRange_RemoveFromSelection, TextRange_RemoveFromSelection function [Windows Accessibility], uiauto.uiauto_TextRange_RemoveFromSelectionConPat, uiauto_TextRange_RemoveFromSelectionConPat, uiautomationcoreapi/TextRange_RemoveFromSelection, winauto.uiauto_TextRange_RemoveFromSelectionConPat
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
 - TextRange_RemoveFromSelection
 - uiautomationcoreapi/TextRange_RemoveFromSelection
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
 - TextRange_RemoveFromSelection
---

# TextRange_RemoveFromSelection function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Removes the selected text, corresponding to the calling text range 
        <i>TextPatternRangeEndpoint_Start</i> 
        and <i>TextPatternRangeEndpoint_End</i> 
        endpoints, from an existing collection of selected text in a text container that supports multiple, disjoint selections.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

The text insertion point will move to the area of the new selection.
            

Providing a degenerate text range will move the text insertion point.