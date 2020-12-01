---
UID: NF:tom.ITextRange2.SetFormattedText2
title: ITextRange2::SetFormattedText2 (tom.h)
description: Sets the text of this range to the formatted text of the specified range.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","SetFormattedText2 method","ITextRange2.SetFormattedText2","ITextRange2::SetFormattedText2","SetFormattedText2","SetFormattedText2 method [Windows Controls]","SetFormattedText2 method [Windows Controls]","ITextRange2 interface","controls.itextrange2_setformattedtext2","tom/ITextRange2::SetFormattedText2"]
old-location: controls\itextrange2_setformattedtext2.htm
tech.root: Controls
ms.assetid: 151be9ee-da5d-4e50-a12e-0473cf1c7d91
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetFormattedText2 method, ITextRange2.SetFormattedText2, ITextRange2::SetFormattedText2, SetFormattedText2, SetFormattedText2 method [Windows Controls], SetFormattedText2 method [Windows Controls],ITextRange2 interface, controls.itextrange2_setformattedtext2, tom/ITextRange2::SetFormattedText2
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextRange2::SetFormattedText2
 - tom/ITextRange2::SetFormattedText2
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
 - ITextRange2.SetFormattedText2
---

# ITextRange2::SetFormattedText2


## -description

Sets the text of this range to the formatted text of the specified range.

## -parameters

### -param pRange [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The range that contains the formatted text that replaces the text of this range.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange2-getformattedtext2">ITextRange2::GetFormattedText2</a>