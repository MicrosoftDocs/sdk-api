---
UID: NF:tom.ITextRange.MoveUntil
title: ITextRange::MoveUntil (tom.h)
author: windows-sdk-content
description: Searches up to Count characters for the first character in the set of characters specified by Cset. If a character is found, the range is collapsed to that point. The start of the search and the direction are also specified by Count.
old-location: controls\ITextRange_MoveUntil.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\moveuntil.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],MoveUntil method, ITextRange.MoveUntil, ITextRange::MoveUntil, MoveUntil, MoveUntil method [Windows Controls], MoveUntil method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveUntil, _win32_ITextRange_MoveUntil_cpp, controls.ITextRange_MoveUntil, controls._win32_ITextRange_MoveUntil, tom/ITextRange::MoveUntil
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
 - ITextRange.MoveUntil
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextRange::MoveUntil


## -description


Searches up to <i>Count</i> characters for the first character in the set of characters specified by <i>Cset</i>. If a character is found, the range is collapsed to that point. The start of the search and the direction are also specified by <i>Count</i>. 


## -parameters




### -param Cset

Type: <b>VARIANT*</b>

The character set used in the match. This could be an explicit string of characters or a character-set index. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">Character Match Sets</a>. 


### -param Count

Type: <b>long</b>

Maximum number of characters to move past. The default value is <b>tomForward</b>, which searches to the end of the story. If <i>Count</i> is less than zero, the search is backward starting at the start position. If <i>Count</i> is greater than zero, the search is forward starting at the end. 


### -param pDelta

Type: <b>long*</b>

The number of characters the insertion point is moved, plus 1 for a match if <i>Count</i> is greater than zero, and –1 for a match if <i>Count</i> less than zero. The pointer can be null. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>Cset</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>
 




## -remarks



If no character is matched, the range is unchanged.

The motion described by <b>ITextRange::MoveUntil</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see the discussion in <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> and the Remarks section of <a href="https://msdn.microsoft.com/en-us/library/Bb774064(v=VS.85).aspx">ITextRange::Move</a>.

The <a href="https://msdn.microsoft.com/en-us/library/Bb774080(v=VS.85).aspx">ITextRange::MoveStartUntil</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb774070(v=VS.85).aspx">ITextRange::MoveEndUntil</a> methods move the start and end, respectively, until it finds the first character that is also in the set specified by the <i>Cset</i> parameter.

The <b>ITextRange::MoveUntil</b> method is similar to <a href="https://msdn.microsoft.com/en-us/library/Bb774088(v=VS.85).aspx">ITextRange::MoveWhile</a>, but there are two differences. First, <b>MoveUntil</b> moves an insertion point <i>until</i> it finds the first character that belongs to the character set specified by <i>Cset</i>. Second, in <b>MoveUntil</b> the character matched counts as an additional character in the value returned in <i>pDelta</i>. This lets you know that the character at one end of the range or the other belongs to the <i>Cset</i> even though the insertion point stays at one of the range ends. 

For example, suppose the range, r, is an insertion point. To see if the character at r (that is, given by r.<a href="https://msdn.microsoft.com/en-us/library/Bb773937(v=VS.85).aspx">GetChar</a>()) is in <i>Cset</i>, call 
				


```
r.MoveUntil(Cset, 1)
```


If the character is in <i>Cset</i>, the return value is 1 and the insertion point does not move. Similarly, to see if the character preceding r is in <i>Cset</i>, call 

				


```
r.MoveUntil(Cset, -1)
```


If the character is in <i>Cset</i>, the return value is –1.

The following Microsoft Visual Basic for Applications (VBA) subroutine prints all numbers in the story identified by the range, r.
				


```
Sub PrintNumbers (r As ITextRange)
   r.SetRange 0, 0    // r = insertion point at start of story
   While r.MoveUntil(C1_DIGIT)  // Move r to 1st digit in next number
      r.MoveEndWhile C1_DIGIT  // Select number (span of digits)
      Print r    // Print it
   Wend
End Sub
```





## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773937(v=VS.85).aspx">GetChar</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774064(v=VS.85).aspx">Move</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774070(v=VS.85).aspx">MoveEndUntil</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774080(v=VS.85).aspx">MoveStartUntil</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774088(v=VS.85).aspx">MoveWhile</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

