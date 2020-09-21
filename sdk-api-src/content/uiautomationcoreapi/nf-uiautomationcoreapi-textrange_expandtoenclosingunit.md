---
UID: NF:uiautomationcoreapi.TextRange_ExpandToEnclosingUnit
title: TextRange_ExpandToEnclosingUnit function (uiautomationcoreapi.h)
description: Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.
helpviewer_keywords: ["TextRange_ExpandToEnclosingUnit","TextRange_ExpandToEnclosingUnit function [Windows Accessibility]","uiauto.uiauto_TextRange_ExpandToEnclosingUnitConPat","uiauto_TextRange_ExpandToEnclosingUnitConPat","uiautomationcoreapi/TextRange_ExpandToEnclosingUnit","winauto.uiauto_TextRange_ExpandToEnclosingUnitConPat"]
old-location: winauto\uiauto_TextRange_ExpandToEnclosingUnitConPat.htm
tech.root: WinAuto
ms.assetid: a95a4e34-d3b3-4aa0-a21e-9788874dcf9b
ms.date: 12/05/2018
ms.keywords: TextRange_ExpandToEnclosingUnit, TextRange_ExpandToEnclosingUnit function [Windows Accessibility], uiauto.uiauto_TextRange_ExpandToEnclosingUnitConPat, uiauto_TextRange_ExpandToEnclosingUnitConPat, uiautomationcoreapi/TextRange_ExpandToEnclosingUnit, winauto.uiauto_TextRange_ExpandToEnclosingUnitConPat
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
 - TextRange_ExpandToEnclosingUnit
 - uiautomationcoreapi/TextRange_ExpandToEnclosingUnit
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
 - TextRange_ExpandToEnclosingUnit
---

# TextRange_ExpandToEnclosingUnit function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param unit [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

The unit that the provider must expand the text range to.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

If the range is already an integral number of the specified units, it remains unchanged.

If the starting endpoint is not at a <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a> boundary, it is moved backward until it is at a boundary. 
			Subsequently, if the ending endpoint is not at a boundary, or if it is at the same boundary as the starting endpoint, 
			the ending endpoint is moved forward until it is at a boundary.

<div class="alert"><b>Note</b>  It is common for a screen reader to read out a full word, entire paragraph, and so on, 
			at the insertion point or any virtual cursor position.
</div>
<div> </div>
<b>TextRange_ExpandToEnclosingUnit</b> respects both hidden and visible text. The UI Automationclient can check the is-hidden attribute (Text_IsHidden_Attribute_GUID) for text visibility.

<b>TextRange_ExpandToEnclosingUnit</b> defaults up to the next supported <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a> if the given <b>TextUnit</b> is not supported by the control.