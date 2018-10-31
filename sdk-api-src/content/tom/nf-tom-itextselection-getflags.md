---
UID: NF:tom.ITextSelection.GetFlags
title: ITextSelection::GetFlags
author: windows-sdk-content
description: Gets the text selection flags.
old-location: controls\ITextSelection_GetFlags.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getflags.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetFlags, GetFlags method [Windows Controls], GetFlags method [Windows Controls],ITextSelection interface, ITextSelection interface [Windows Controls],GetFlags method, ITextSelection.GetFlags, ITextSelection::GetFlags, _win32_ITextSelection_GetFlags, _win32_ITextSelection_GetFlags_cpp, controls.ITextSelection_GetFlags, controls._win32_ITextSelection_GetFlags, tom/ITextSelection::GetFlags
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
 - ITextSelection.GetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextSelection::GetFlags


## -description


Gets the text selection flags.


## -parameters




### -param pFlags

Type: <b>long*</b>

Any combination of the following selection flags.
               

<table class="clsStd">
<tr>
<th>Selection Flag</th>
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

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pFlags</i> is null, the method fails and it returns E_INVALIDARG.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774060(v=VS.85).aspx">ITextSelection</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774143(v=VS.85).aspx">SetFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

