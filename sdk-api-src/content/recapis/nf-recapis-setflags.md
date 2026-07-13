---
UID: NF:recapis.SetFlags
title: SetFlags function (recapis.h)
description: Specifies how the recognizer interprets the ink and determines the result string.Call this function before processing the ink for the first time. Therefore, call the SetFlags function before calling the Process function.
helpviewer_keywords: ["62ad43c4-4795-4af9-af20-e45da30ba132","RECOFLAG_AUTOSPACE","RECOFLAG_COERCE","RECOFLAG_LINEMODE","RECOFLAG_PREFIXOK","RECOFLAG_SINGLESEG","RECOFLAG_WORDMODE","SetFlags","SetFlags function [Tablet PC]","recapis/SetFlags","tablet.setflags"]
old-location: tablet\setflags.htm
tech.root: tablet
ms.assetid: 62ad43c4-4795-4af9-af20-e45da30ba132
ms.date: 12/05/2018
ms.keywords: 62ad43c4-4795-4af9-af20-e45da30ba132, RECOFLAG_AUTOSPACE, RECOFLAG_COERCE, RECOFLAG_LINEMODE, RECOFLAG_PREFIXOK, RECOFLAG_SINGLESEG, RECOFLAG_WORDMODE, SetFlags, SetFlags function [Tablet PC], recapis/SetFlags, tablet.setflags
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetFlags
 - recapis/SetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - SetFlags
---

# SetFlags function


## -description

Specifies how the recognizer interprets the ink and determines the result string.

Call this function before processing the ink for the first time. Therefore, call the <b>SetFlags</b> function before calling the <a href="/windows/desktop/api/recapis/nf-recapis-process">Process</a> function.

## -parameters

### -param hrc [in]

Handle to the recognizer context.

### -param dwFlags [in]

The following table lists the flags that you may set to specify how the recognizer interprets the ink and determines the result string. Use the <b>OR</b> operator (|) to combine flags as appropriate.



<table>
<tr>
<th>Bit flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECOFLAG_AUTOSPACE"></a><a id="recoflag_autospace"></a><dl>
<dt><b>RECOFLAG_AUTOSPACE</b></dt>
</dl>
</td>
<td width="60%">
Recognizer uses smart spacing based on language model rules.

</td>
</tr>
<tr>
<td width="40%"><a id="RECOFLAG_COERCE"></a><a id="recoflag_coerce"></a><dl>
<dt><b>RECOFLAG_COERCE</b></dt>
</dl>
</td>
<td width="60%">
Recognizer coerces the result based on the factoid you specify for the context. For example, if you specify a phone number factoid and the user enters the word "hello", the recognizer may return a random phone number or an empty string. If you do not specify this flag, the recognizer returns "hello" as the result.


</td>
</tr>
<tr>
<td width="40%"><a id="RECOFLAG_PREFIXOK"></a><a id="recoflag_prefixok"></a><dl>
<dt><b>RECOFLAG_PREFIXOK</b></dt>
</dl>
</td>
<td width="60%">
Recognizer supports the recognition of any prefix part of the strings that are defined in the default or specified (factoid) language model.

For example, without this flag, the user writes "handw" and the recognizer returns suggestions (such as "hander" or "handed") that are words that exist in the recognizer lexicon. With the flag, the recognizer may return "handw" as one of the suggestions since it is a valid prefix of the word "handwriting" that exists in the recognizer lexicon.

The Tablet PC Input Panel sets this flag in most cases, except when the input scope is IS_DEFAULT (or no input scope) or when there is no user word list or regular expression.

Recognizers of East Asian characters should return E_INVALIDARG when a caller passes in this flag.


</td>
</tr>
<tr>
<td width="40%"><a id="RECOFLAG_LINEMODE"></a><a id="recoflag_linemode"></a><dl>
<dt><b>RECOFLAG_LINEMODE</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not split lines but must still do character and word separation. This is the same as lined mode, except that there is no guide, and all ink is assumed to be in a single line. When this flag is set, a guide, if set, is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="RECOFLAG_SINGLESEG"></a><a id="recoflag_singleseg"></a><dl>
<dt><b>RECOFLAG_SINGLESEG</b></dt>
</dl>
</td>
<td width="60%">
Disables multiple segmentation. By default, the recognizer returns multiple segmentations (alternates) for the ink.

For example, if you write "together" as separate strokes, the recognizer may segment the ink as "to get her", "to gather", or "together". Set this flag if you do not need multiple segmentations of the ink when you query for alternates. This improves performance and reduces memory usage.


</td>
</tr>
<tr>
<td width="40%"><a id="RECOFLAG_WORDMODE"></a><a id="recoflag_wordmode"></a><dl>
<dt><b>RECOFLAG_WORDMODE</b></dt>
</dl>
</td>
<td width="60%">
Recognizer treats the ink as a single word. For example, if the context contains "to get her", the recognizer returns "together".

</td>
</tr>
</table>

## -returns

This function can return one of these values.

<table>
<tr>
<th>HRESULT value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The context is invalid or one of the parameters is an invalid pointer.

</td>
</tr>
</table>

## -remarks

Prior to Microsoft Windows XP Tablet PC Edition Development Kit 1.7, Tablet PC Input Panel performed smart spacing. Starting with Tablet PC SDK 1.7, Input Panel continues to produce results with preliminary spacing recommendations. Tablet PC Input Panel's spacing results may however be changed by the recognizer's recommendations (results). The recognizer is able to do this by using text contextual information (based on the <a href="/windows/desktop/api/recapis/nf-recapis-settextcontext">SetTextContext</a> call made by Input Panel) and its internal language model rules.

Input Panel is able to determine whether the recognizer is capable of doing auto-spacing by calling this function with the RECOFLAG_AUTOSPACE flag set. If the recognizer does not support auto-spacing, E_INVALIDARG is returned.

<div class="alert"><b>Note</b>  Only line mode is supported in the <b>SetFlags</b> function. Boxed mode, free mode, and single-line mode are not supported.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-setfactoid">SetFactoid Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-settextcontext">SetTextContext Function</a>