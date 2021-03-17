---
UID: NF:tom.ITextStrings.SuffixTop
title: ITextStrings::SuffixTop (tom.h)
description: Suffixes a string to the top string in the collection.
helpviewer_keywords: ["ITextStrings interface [Windows Controls]","SuffixTop method","ITextStrings.SuffixTop","ITextStrings::SuffixTop","SuffixTop","SuffixTop method [Windows Controls]","SuffixTop method [Windows Controls]","ITextStrings interface","controls.itextstrings_suffixtop","tom/ITextStrings::SuffixTop"]
old-location: controls\itextstrings_suffixtop.htm
tech.root: Controls
ms.assetid: 66f4e5c6-e97b-48a5-9c71-3efb1eba12d6
ms.date: 12/05/2018
ms.keywords: ITextStrings interface [Windows Controls],SuffixTop method, ITextStrings.SuffixTop, ITextStrings::SuffixTop, SuffixTop, SuffixTop method [Windows Controls], SuffixTop method [Windows Controls],ITextStrings interface, controls.itextstrings_suffixtop, tom/ITextStrings::SuffixTop
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
 - ITextStrings::SuffixTop
 - tom/ITextStrings::SuffixTop
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
 - ITextStrings.SuffixTop
---

# ITextStrings::SuffixTop


## -description

Suffixes a string to the top string in the collection.

## -parameters

### -param bstr [in]

Type: <b>BSTR</b>

The text to suffix to the top string.

### -param pRange [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The range with the desired character formatting.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

## -remarks

This method is similar to <a href="/windows/desktop/api/tom/nf-tom-itextstrings-append">ITextStrings::Append</a>, but appends a string instead of a range.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>