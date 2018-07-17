---
UID: NF:tom.ITextRange.FindTextEnd
title: ITextRange::FindTextEnd
author: windows-sdk-content
description: Searches up to Count characters for the string, bstr, starting from the range's End cp.
old-location: controls\ITextRange_FindTextEnd.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\findtextend.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FindTextEnd, FindTextEnd method [Windows Controls], FindTextEnd method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],FindTextEnd method, ITextRange.FindTextEnd, ITextRange::FindTextEnd, _win32_ITextRange_FindTextEnd, _win32_ITextRange_FindTextEnd_cpp, controls.ITextRange_FindTextEnd, controls._win32_ITextRange_FindTextEnd, tom/ITextRange::FindTextEnd
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.FindTextEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::FindTextEnd


## -description


Searches up to <i>Count</i> characters for the string, <i>bstr</i>, starting from the range's End <i>cp</i>. The search is subject to the comparison parameter, <i>Flags</i>. If the string is found, the End <i>cp</i> is changed to be the end of the matched string, and <i>pLength</i> is set equal to the length of the string. If the string is not found, the range is unchanged and <i>pLength</i> is set equal to zero.


## -parameters




### -param bstr

Type: <b>BSTR</b>

String to search for.


### -param Count

Type: <b>long</b>

Maximum number of characters to search. It can be one of the following. 
					

<table class="clsStd">
<tr>
<td><i>tomForward</i></td>
<td>Search to the end of the story. This is the default value.</td>
</tr>
<tr>
<td><i>n</i> (greater than 0)</td>
<td>Search forward for <i>n</i> chars, starting from <i>cpLim.</i></td>
</tr>
<tr>
<td><i>n</i> (less than 0)</td>
<td>Search backward for 
								<i>n</i> chars, starting from 
								<i>cpLim.</i></td>
</tr>
</table>
 


### -param Flags

Type: <b>long</b>

Flags governing comparisons. It can be zero (the default) or any combination of the following values. 
					

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

The length of string matched. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb787783(v=VS.85).aspx">FindText</a>



<a href="https://msdn.microsoft.com/library/Bb773923(v=VS.85).aspx">FindTextStart</a>



<a href="https://msdn.microsoft.com/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

