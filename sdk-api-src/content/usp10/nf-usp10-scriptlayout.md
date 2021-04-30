---
UID: NF:usp10.ScriptLayout
title: ScriptLayout function (usp10.h)
description: Converts an array of run embedding levels to a map of visual-to-logical position and/or logical-to-visual position.
helpviewer_keywords: ["ScriptLayout","ScriptLayout function [Internationalization for Windows Applications]","_win32_ScriptLayout","intl.scriptlayout","usp10/ScriptLayout"]
old-location: intl\scriptlayout.htm
tech.root: Intl
ms.assetid: 6f3c74af-8d7f-4c66-8a11-6408a6897cbe
ms.date: 12/05/2018
ms.keywords: ScriptLayout, ScriptLayout function [Internationalization for Windows Applications], _win32_ScriptLayout, intl.scriptlayout, usp10/ScriptLayout
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - ScriptLayout
 - usp10/ScriptLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptLayout
---

# ScriptLayout function


## -description

Converts an array of run <a href="/windows/desktop/Intl/uniscribe-glossary">embedding levels</a> to a map of visual-to-logical position and/or logical-to-visual position.

## -parameters

### -param cRuns [in]

Number of runs to process.

### -param pbLevel [in]

Pointer to an array, of length indicated by <i>cRuns</i>, containing run embedding levels. Embedding levels for all runs on the line must be included, ordered logically. For more information, see the Remarks section.

### -param piVisualToLogical [out, optional]

Pointer to an array, of length indicated by <i>cRuns</i>, in which this function retrieves the run embedding levels reordered to visual order. The first array element represents the run to display at the far left, and subsequent entries should be displayed progressing from left to right. The function sets this parameter to <b>NULL</b> if there is no output.

### -param piLogicalToVisual [out, optional]

Pointer to an array, of length indicated by <i>cRuns</i>, in which this function retrieves the visual run positions. The first array element is the relative visual position where the first logical run should be displayed, the leftmost display position being 0. The function sets this parameter to <b>NULL</b> if there is no output.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

This function handles only data that pertains to a single line of text.

The run embedding levels are defined in the Unicode bidirectional algorithm. They describe the direction of a run, the direction of any runs in which it is embedded, and the direction of the paragraph. No other input is required for the call to this function. For more information, see <a href="/windows/desktop/Intl/unicode">Unicode</a>.

The following table lists the predefined embedding levels. The application can add levels as needed.

<table>
<tr>
<th>Level</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>A left-to-right run in a left-to-right paragraph.</td>
</tr>
<tr>
<td>1</td>
<td>A right-to-left run embedded in a left-to-right run in a left-to-right paragraph. Alternatively, a right-to-left run, not embedded in another run, in a right-to-left paragraph.</td>
</tr>
<tr>
<td>2</td>
<td>A left-to-right run embedded in a right-to-left run of type 1.</td>
</tr>
<tr>
<td>3</td>
<td>A right-to-left run embedded in a left-to-right run of type 2.</td>
</tr>
</table>
 

A "logical position" refers to the placement of a run relative to other runs. It is the position in a backing store, and corresponds to the order in which the user reads the text aloud. The "visual position" of a run refers to the way the run is visually displayed on the line, taking into account the possible directions that the run can have.

The application can call this function setting either <i>piLogicalToVisual</i> or <i>piVisualToLogical</i>, or both.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>