---
UID: NF:tom.ITextRange.MoveWhile
title: ITextRange::MoveWhile
author: windows-sdk-content
description: Starts at a specified end of a range and searches while the characters belong to the set specified by Cset and while the number of characters is less than or equal to Count.
old-location: controls\ITextRange_MoveWhile.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\movewhile.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextRange interface [Windows Controls],MoveWhile method, ITextRange.MoveWhile, ITextRange::MoveWhile, MoveWhile, MoveWhile method [Windows Controls], MoveWhile method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveWhile, _win32_ITextRange_MoveWhile_cpp, controls.ITextRange_MoveWhile, controls._win32_ITextRange_MoveWhile, tom/ITextRange::MoveWhile
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
 - ITextRange.MoveWhile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::MoveWhile


## -description


Starts at a specified end of a range and searches while the characters belong to the set specified by <i>Cset</i> and while the number of characters is less than or equal to <i>Count</i>. The range is collapsed to an insertion point when a non-matching character is found.


## -parameters




### -param Cset

Type: <b>VARIANT*</b>

The character set to use in the match. This could be an explicit string of characters or a character-set index. For more information, see <a href="About_Text_Object_Model.htm">Character Match Sets</a>. 


### -param Count

Type: <b>long</b>

Maximum number of characters to move past. The default value is <b>tomForward</b>, which searches to the end of the story. If <i>Count</i> is less than zero, the search starts at the start position and goes backward — toward the beginning of the story. If <i>Count</i> is greater than zero, the search starts at the end position and goes forward — toward the end of the story. 


### -param pDelta

Type: <b>long*</b>

The actual count of characters end is moved. This parameter can be null. 


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
Cset is not valid.

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



The motion described by <a href="https://msdn.microsoft.com/a35bdd47-fa5c-4260-8d99-14b0bd4694dd">ITextRange::MoveUntil</a> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see the discussion in <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> and the Remarks section of <a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">ITextRange::Move</a>.

The <b>ITextRange::MoveWhile</b> method is similar to <a href="https://msdn.microsoft.com/a35bdd47-fa5c-4260-8d99-14b0bd4694dd">ITextRange::MoveUntil</a>, but <b>MoveWhile</b> searches as long as it finds members of the set specified by <i>Cset</i>, and there is no additional increment to the value <i>pDelta</i>.

The <a href="https://msdn.microsoft.com/5b55abd6-7f1e-499e-8794-6ccb7141ddbb">ITextRange::MoveStartWhile</a> and <a href="https://msdn.microsoft.com/b4559270-5676-40da-be21-31367607c7b7">ITextRange::MoveEndWhile</a> methods move the start and end, respectively, just past all contiguous characters that are found in set of characters specified by the <i>Cset</i> parameter.

The <b>VARIANT</b> type is primarily intended to be used with <b>IDispatch</b> scenarios like Microsoft Visual Basic for Applications (VBA), but it can be readily used from C or C++ as well. The following C++ code illustrates how to initialize and use the <b>VARIANT</b> argument  for matching a span of digits in the range r.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>VariantInit(&amp;varg);
varg.vt = VT_I4;
varg.lVal = C1_DIGIT;
hr = r.MoveWhile(&amp;varg, tomForward, pDelta); // Move IP past span of digits
</pre>
</td>
</tr>
</table></span></div>
Alternatively, an explicit string could be used, as in the following sample.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>VariantInit(&amp;varg);
bstr = SysAllocString("0123456789");
varg.vt = VT_BSTR;
varg.bstr = bstr;
hr =r.MoveWhile(&amp;varg, tomForward, pDelta);    // Move IP past span of digits
</pre>
</td>
</tr>
</table></span></div>
The following VBA example code matches the body of the next Standard Generalized Markup Language (SGML) entry in a range, r. SGML entries start with &lt;
				<code>keyword ...</code>&gt; and end with &lt;/
				<code>keyword</code>&gt;. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>r.Find &lt;                  // Get to start of next tag
r.MoveWhile C1_SPACE      // Bypass any space characters
r.MoveEndWhile C1_ALPHA   // Match keyword
s$ = &lt;/ + r               // Create VBA string to search for
r.Find &gt;                  // Bypass remainder of start tag
r.FindEnd s$              // Match up to end of closing keyword
r.FindEnd &lt;, tomStart     // Back up to start of end tag
                          // r has body of SGML entry
                           </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">Move</a>



<a href="https://msdn.microsoft.com/b4559270-5676-40da-be21-31367607c7b7">MoveEndWhile</a>



<a href="https://msdn.microsoft.com/5b55abd6-7f1e-499e-8794-6ccb7141ddbb">MoveStartWhile</a>



<a href="https://msdn.microsoft.com/a35bdd47-fa5c-4260-8d99-14b0bd4694dd">MoveUntil</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

