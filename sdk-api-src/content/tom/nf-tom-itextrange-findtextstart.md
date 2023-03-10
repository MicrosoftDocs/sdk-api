---
UID: NF:tom.ITextRange.FindTextStart
title: ITextRange::FindTextStart (tom.h)
description: Searches up to Count characters for the string, bstr, starting at the range's Start cp (cpFirst).
helpviewer_keywords: ["FindTextStart","FindTextStart method [Windows Controls]","FindTextStart method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","FindTextStart method","ITextRange.FindTextStart","ITextRange::FindTextStart","_win32_ITextRange_FindTextStart","_win32_ITextRange_FindTextStart_cpp","controls.ITextRange_FindTextStart","controls._win32_ITextRange_FindTextStart","tom/ITextRange::FindTextStart"]
old-location: controls\ITextRange_FindTextStart.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\findtextstart.htm
ms.date: 12/05/2018
ms.keywords: FindTextStart, FindTextStart method [Windows Controls], FindTextStart method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],FindTextStart method, ITextRange.FindTextStart, ITextRange::FindTextStart, _win32_ITextRange_FindTextStart, _win32_ITextRange_FindTextStart_cpp, controls.ITextRange_FindTextStart, controls._win32_ITextRange_FindTextStart, tom/ITextRange::FindTextStart
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRange::FindTextStart
 - tom/ITextRange::FindTextStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.FindTextStart
---

# ITextRange::FindTextStart


## -description

Searches up to <i>Count</i> characters for the string, <i>bstr</i>, starting at the range's Start <i>cp</i> (<i>cpFirst)</i>. The search is subject to the comparison parameter, <i>Flags</i>. If the string is found, the Start <i>cp</i> is changed to the matched string, and <i>pLength</i> is set equal to the length of the string. If the string is not found, the range is unchanged, and <i>pLength</i> is set equal to zero.

## -parameters

### -param bstr

Type: <b>BSTR</b>

The string to search for.

### -param Count

Type: <b>long</b>

Maximum number of characters to search. It can be one of the following. 
					

<table class="clsStd">
<tr>
<td><i>tomForward</i></td>
<td>Search to the end of the story. This is the default value.</td>
</tr>
<tr>
<td><i>n </i>(greater than 0)</td>
<td>Search forward for <i>n</i> chars, starting from <i>cpLim.</i></td>
</tr>
<tr>
<td><i>n </i>(less than 0)</td>
<td>Search backward for <i>n</i> chars, starting from <i>cpLim.</i></td>
</tr>
</table>

### -param Flags

Type: <b>long</b>

Flags governing the comparisons. It can be zero (the default) or any combination of the following values. 
					

<table class="clsStd">
<tr>
<td><i>tomMatchWord</i></td>
<td>2</td>
<td>Matches whole words.</td>
</tr>
<tr>
<td><i>tomMatchCase</i></td>
<td>4</td>
<td>Matches case.</td>
</tr>
<tr>
<td><i>tomMatchPattern</i></td>
<td>8</td>
<td>Matches regular expressions.</td>
</tr>
</table>

### -param pLength

Type: <b>long*</b>

The length of the matched string.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-findtext">FindText</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-findtextend">FindTextEnd</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>