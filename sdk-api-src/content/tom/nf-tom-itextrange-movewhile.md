---
UID: NF:tom.ITextRange.MoveWhile
title: ITextRange::MoveWhile (tom.h)
description: Starts at a specified end of a range and searches while the characters belong to the set specified by Cset and while the number of characters is less than or equal to Count.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","MoveWhile method","ITextRange.MoveWhile","ITextRange::MoveWhile","MoveWhile","MoveWhile method [Windows Controls]","MoveWhile method [Windows Controls]","ITextRange interface","_win32_ITextRange_MoveWhile","_win32_ITextRange_MoveWhile_cpp","controls.ITextRange_MoveWhile","controls._win32_ITextRange_MoveWhile","tom/ITextRange::MoveWhile"]
old-location: controls\ITextRange_MoveWhile.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\movewhile.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],MoveWhile method, ITextRange.MoveWhile, ITextRange::MoveWhile, MoveWhile, MoveWhile method [Windows Controls], MoveWhile method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveWhile, _win32_ITextRange_MoveWhile_cpp, controls.ITextRange_MoveWhile, controls._win32_ITextRange_MoveWhile, tom/ITextRange::MoveWhile
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
 - ITextRange::MoveWhile
 - tom/ITextRange::MoveWhile
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
 - ITextRange.MoveWhile
---

# ITextRange::MoveWhile


## -description

Starts at a specified end of a range and searches while the characters belong to the set specified by <i>Cset</i> and while the number of characters is less than or equal to <i>Count</i>. The range is collapsed to an insertion point when a non-matching character is found.

## -parameters

### -param Cset

Type: <b>VARIANT*</b>

The character set to use in the match. This could be an explicit string of characters or a character-set index. For more information, see <a href="/windows/desktop/Controls/about-text-object-model">Character Match Sets</a>.

### -param Count

Type: <b>long</b>

Maximum number of characters to move past. The default value is <b>tomForward</b>, which searches to the end of the story. If <i>Count</i> is less than zero, the search starts at the start position and goes backward — toward the beginning of the story. If <i>Count</i> is greater than zero, the search starts at the end position and goes forward — toward the end of the story.

### -param pDelta

Type: <b>long*</b>

The actual count of characters end is moved. This parameter can be null.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

The motion described by <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveuntil">ITextRange::MoveUntil</a> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see the discussion in <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> and the Remarks section of <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a>.

The <b>ITextRange::MoveWhile</b> method is similar to <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveuntil">ITextRange::MoveUntil</a>, but <b>MoveWhile</b> searches as long as it finds members of the set specified by <i>Cset</i>, and there is no additional increment to the value <i>pDelta</i>.

The <a href="/windows/desktop/api/tom/nf-tom-itextrange-movestartwhile">ITextRange::MoveStartWhile</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveendwhile">ITextRange::MoveEndWhile</a> methods move the start and end, respectively, just past all contiguous characters that are found in set of characters specified by the <i>Cset</i> parameter.

The <b>VARIANT</b> type is primarily intended to be used with <b>IDispatch</b> scenarios like Microsoft Visual Basic for Applications (VBA), but it can be readily used from C or C++ as well. The following C++ code illustrates how to initialize and use the <b>VARIANT</b> argument  for matching a span of digits in the range r.


```
VariantInit(&varg);
varg.vt = VT_I4;
varg.lVal = C1_DIGIT;
hr = r.MoveWhile(&varg, tomForward, pDelta); // Move IP past span of digits

```


Alternatively, an explicit string could be used, as in the following sample.


```
VariantInit(&varg);
bstr = SysAllocString("0123456789");
varg.vt = VT_BSTR;
varg.bstr = bstr;
hr =r.MoveWhile(&varg, tomForward, pDelta);    // Move IP past span of digits

```


The following VBA example code matches the body of the next Standard Generalized Markup Language (SGML) entry in a range, r. SGML entries start with &lt;
				<code>keyword ...</code>&gt; and end with &lt;/
				<code>keyword</code>&gt;. 


```
r.Find <                  // Get to start of next tag
r.MoveWhile C1_SPACE      // Bypass any space characters
r.MoveEndWhile C1_ALPHA   // Match keyword
s$ = </ + r               // Create VBA string to search for
r.Find >                  // Bypass remainder of start tag
r.FindEnd s$              // Match up to end of closing keyword
r.FindEnd <, tomStart     // Back up to start of end tag
                          // r has body of SGML entry
                           
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-moveendwhile">MoveEndWhile</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-movestartwhile">MoveStartWhile</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-moveuntil">MoveUntil</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>