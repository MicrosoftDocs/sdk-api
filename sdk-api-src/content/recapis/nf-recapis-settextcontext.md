---
UID: NF:recapis.SetTextContext
title: SetTextContext function (recapis.h)
description: Provides the text strings that come before and after the text contained in the recognizer context.You call this function before processing the ink for the first time. Therefore, call the SetTextContext function before calling the Process function.
helpviewer_keywords: ["SetTextContext","SetTextContext function [Tablet PC]","f5461326-3def-4564-81ea-32a63b889da0","recapis/SetTextContext","tablet.settextcontext"]
old-location: tablet\settextcontext.htm
tech.root: tablet
ms.assetid: f5461326-3def-4564-81ea-32a63b889da0
ms.date: 12/05/2018
ms.keywords: SetTextContext, SetTextContext function [Tablet PC], f5461326-3def-4564-81ea-32a63b889da0, recapis/SetTextContext, tablet.settextcontext
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
 - SetTextContext
 - recapis/SetTextContext
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
 - SetTextContext
---

# SetTextContext function


## -description

Provides the text strings that come before and after the text contained in the recognizer context.

You call this function before processing the ink for the first time. Therefore, call the <b>SetTextContext</b> function before calling the <a href="/windows/desktop/api/recapis/nf-recapis-process">Process</a> function.

## -parameters

### -param hrc

Handle to the recognizer context.

### -param cwcBefore

Number of characters in <i>pwcBefore</i>.

### -param pwcBefore

Text string that comes before the text contained in the recognizer context. The string is not <b>NULL</b> terminated.

### -param cwcAfter

Number of characters in <i>pwcAfter</i>.

### -param pwcAfter

Text string that comes after the text contained in the recognizer context. The string is not <b>NULL</b> -terminated.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The context is invalid or one of the parameters is an invalid pointer.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was specified.

</td>
</tr>
</table>

## -remarks

The <b>SetTextContext</b> function provides context for a phrase or a word, increasing your recognizer's accuracy. For example, if the <i>pwcBefore</i><i>pwcBefore</i> string is "under the " and the <i>pwcAfter</i> string is "in the house", you can bias your recognizer using a word or words between the strings. Your recognizer should consider the space after "the" and before "in" when performing the recognition.

However, if the <i>pwcAfter</i> string is "Hel" and the <i>pwcBefore</i> string is "o", the lack of space between the strings indicates the recognizer should recognize one or more letters inside a word that begins with "Hel" and ends with "o".

It is recommended that you limit the length of the text context to no more than 1024 characters each for the left and right contexts.