---
UID: NF:tom.ITextRange.FindTextStart
title: ITextRange::FindTextStart
author: windows-sdk-content
description: Searches up to Count characters for the string, bstr, starting at the range's Start cp (cpFirst).
old-location: controls\ITextRange_FindTextStart.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\findtextstart.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FindTextStart, FindTextStart method [Windows Controls], FindTextStart method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],FindTextStart method, ITextRange.FindTextStart, ITextRange::FindTextStart, _win32_ITextRange_FindTextStart, _win32_ITextRange_FindTextStart_cpp, controls.ITextRange_FindTextStart, controls._win32_ITextRange_FindTextStart, tom/ITextRange::FindTextStart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.FindTextStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextRange.FindTextStart
: 
---

# ITextRange::FindTextStart


## -description


Searches up to <i>Count</i> characters for the string, <i>bstr</i>, starting at the range's Start 

			<i>cp</i> (<i>cpFirst)</i>. The search is subject to the comparison parameter, <i>Flags</i>. If the string is found, the Start 
			<i>cp</i> is changed to the matched string, and <i>pLength</i> is set equal to the length of the string. If the string is not found, the range is unchanged, and <i>pLength</i> is set equal to zero.


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
<td>Search forward for 
								<i>n</i> chars, starting from 
								<i>cpLim.</i></td>
</tr>
<tr>
<td><i>n </i>(less than 0)</td>
<td>Search backward for 
								<i>n</i> chars, starting from 
								<i>cpLim.</i></td>
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



<a href="https://msdn.microsoft.com/e0c95f5b-e147-4c1f-ae1a-def36b0be5c1">FindText</a>



<a href="https://msdn.microsoft.com/2d4ebabf-973d-467f-a80e-80c8abf5194e">FindTextEnd</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

