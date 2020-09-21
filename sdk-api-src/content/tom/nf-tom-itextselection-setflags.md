---
UID: NF:tom.ITextSelection.SetFlags
title: ITextSelection::SetFlags (tom.h)
description: Sets the text selection flags.
helpviewer_keywords: ["ITextSelection interface [Windows Controls]","SetFlags method","ITextSelection.SetFlags","ITextSelection::SetFlags","SetFlags","SetFlags method [Windows Controls]","SetFlags method [Windows Controls]","ITextSelection interface","_win32_ITextSelection_SetFlags","_win32_ITextSelection_SetFlags_cpp","controls.ITextSelection_SetFlags","controls._win32_ITextSelection_SetFlags","tom/ITextSelection::SetFlags"]
old-location: controls\ITextSelection_SetFlags.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setflags.htm
ms.date: 12/05/2018
ms.keywords: ITextSelection interface [Windows Controls],SetFlags method, ITextSelection.SetFlags, ITextSelection::SetFlags, SetFlags, SetFlags method [Windows Controls], SetFlags method [Windows Controls],ITextSelection interface, _win32_ITextSelection_SetFlags, _win32_ITextSelection_SetFlags_cpp, controls.ITextSelection_SetFlags, controls._win32_ITextSelection_SetFlags, tom/ITextSelection::SetFlags
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
 - ITextSelection::SetFlags
 - tom/ITextSelection::SetFlags
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
 - ITextSelection.SetFlags
---

# ITextSelection::SetFlags


## -description

Sets the text selection flags.

## -parameters

### -param Flags

Type: <b>long</b>

New flag values. It can be any combination of the following. 
					

<table class="clsStd">
<tr>
<th>Selection flag</th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomSelStartActive</b></td>
<td>1</td>
<td>Start end is active.</td>
</tr>
<tr>
<td><b>tomSelAtEOL</b></td>
<td>2</td>
<td>For degenerate selections, the ambiguous 
								character position corresponding to both the beginning of a line and the end of the preceding line should have the caret displayed at the end of the preceding line.</td>
</tr>
<tr>
<td><b>tomSelOvertype</b></td>
<td>4</td>
<td>Insert/Overtype mode is set to overtype. </td>
</tr>
<tr>
<td><b>tomSelActive</b></td>
<td>8</td>
<td>Selection is active.</td>
</tr>
<tr>
<td><b>tomSelReplace</b></td>
<td>16</td>
<td>Typing and pasting replaces selection.</td>
</tr>
</table>
 

Each of the table values is binary. Thus, if any value is not set, the text selection has the opposite property.

## -returns

Type: <b>HRESULT</b>

The method returns <b>S_OK</b>.

## -remarks

To make sure that the start end is active and that the ambiguous 
				character position is displayed at the end of the line, execute the following code: 


```
selection.Flags = tomSelStartActive + tomSelAtEOL
```


The 
				Flags property is useful because an <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object can select itself. With <b>SetFlags</b>, you can change the active end from the default value of End, select the caret position for an ambiguous 
				character position, or change the Insert/Overtype mode.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-getflags">GetFlags</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>