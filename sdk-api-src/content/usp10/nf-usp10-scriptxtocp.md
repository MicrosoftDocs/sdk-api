---
UID: NF:usp10.ScriptXtoCP
title: ScriptXtoCP function (usp10.h)
description: Generates the leading or trailing edge of a logical character cluster from the x offset of a run.
helpviewer_keywords: ["ScriptXtoCP","ScriptXtoCP function [Internationalization for Windows Applications]","_win32_ScriptXtoCP","intl.scriptxtocp","usp10/ScriptXtoCP"]
old-location: intl\scriptxtocp.htm
tech.root: Intl
ms.assetid: 98548d60-4cbd-4808-8027-1d8058c41d6d
ms.date: 12/05/2018
ms.keywords: ScriptXtoCP, ScriptXtoCP function [Internationalization for Windows Applications], _win32_ScriptXtoCP, intl.scriptxtocp, usp10/ScriptXtoCP
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
 - ScriptXtoCP
 - usp10/ScriptXtoCP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptXtoCP
---

# ScriptXtoCP function


## -description

Generates the leading or trailing edge of a logical character cluster from the x offset of a run.

## -parameters

### -param iX [in]

Offset, in logical units, from the end of the run specified by the <b>fLogicalOrder</b> member of the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure indicated by the <i>psa</i> parameter.

### -param cChars [in]

Count of logical code points in the run.

### -param cGlyphs [in]

Count of glyphs in the run.

### -param pwLogClust [in]

Pointer to an array of logical clusters.

### -param psva [in]

Pointer to an array of <a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a> structures containing the visual attributes for the glyph.

### -param piAdvance [in]

Pointer to an array of advance widths.

### -param psa [in]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure. The <b>fLogicalOrder</b> member indicates <b>TRUE</b> to use the leading edge of the run, or <b>FALSE</b> to use the trailing edge.

### -param piCP [out]

Pointer to a buffer in which this function retrieves the character position corresponding to the x coordinate.

### -param piTrailing [out]

Pointer to a buffer in which this function retrieves the distance, in code points, from the leading edge of the logical character to the <i>iX</i> position. If this value is 0, the <i>iX</i> position is at the leading edge of the logical character. For more information, see the Remarks section.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

The values passed to this function normally are the results of earlier calls to other Uniscribe functions. See <a href="/windows/desktop/Intl/managing-caret-placement-and-hit-testing">Managing Caret Placement and Hit Testing</a> for details.

The leading and trailing edges of the logical character are determined by the direction of text in the run (left-to-right or right-to-left). For the left-to-right direction, the leading edge is the same as the left edge. For the right-to-left direction, the leading edge is the right edge.

For scripts in which the caret is conventionally placed in the middle of a cluster, for example, Arabic and Hebrew, the retrieved character position can be for any code point in the line. In this case, the <i>piTrailing</i> parameter is set to either 0 or 1.

For scripts in which the caret is conventionally snapped to the boundaries of a cluster, the retrieved character position is always the position of the first code point in a cluster (considered logically). The <i>piTrailing</i> parameter is set to 0 or to the number of code points in the cluster.

The appropriate caret position for a mouse hit is always the retrieved character position plus the distance indicated by <i>piTrailing</i>.

When <i>iX</i> indicates a position outside the run, <b>ScriptXtoCP</b> acts as if there is an extra infinitely large character beyond each end of the run. This results in the behavior shown in the following table.

<table>
<tr>
<th><i>iX</i> position (outside the run)</th>
<th>Result</th>
</tr>
<tr>
<td>Before the run, that is: <i>iX</i> &lt; 0 if run is left-to-right, or <i>iX</i> &gt;= sum of advances if run is right-to-left</td>
<td>Value of <i>piCP</i> is -1 and value of <i>piTrailing</i> is 0</td>
</tr>
<tr>
<td>After the run, that is: <i>iX</i> &gt;= sum of advances if run is left-to-right, or <i>iX</i> &lt; 0 if run is right-to-left</td>
<td>Value of <i>piCP</i> is value of <i>cChars</i> and value of <i>piTrailing</i> is 1</td>
</tr>
</table>
 

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>