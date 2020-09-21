---
UID: NF:tom.ITextStrings.DeleteRange
title: ITextStrings::DeleteRange (tom.h)
description: Deletes the contents of a given range.
helpviewer_keywords: ["DeleteRange","DeleteRange method [Windows Controls]","DeleteRange method [Windows Controls]","ITextStrings interface","ITextStrings interface [Windows Controls]","DeleteRange method","ITextStrings.DeleteRange","ITextStrings::DeleteRange","controls.itextstrings_deleterange","tom/ITextStrings::DeleteRange"]
old-location: controls\itextstrings_deleterange.htm
tech.root: Controls
ms.assetid: 2dd6312a-77ab-4538-a51b-7de49a5457ff
ms.date: 12/05/2018
ms.keywords: DeleteRange, DeleteRange method [Windows Controls], DeleteRange method [Windows Controls],ITextStrings interface, ITextStrings interface [Windows Controls],DeleteRange method, ITextStrings.DeleteRange, ITextStrings::DeleteRange, controls.itextstrings_deleterange, tom/ITextStrings::DeleteRange
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
 - ITextStrings::DeleteRange
 - tom/ITextStrings::DeleteRange
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
 - ITextStrings.DeleteRange
---

# ITextStrings::DeleteRange


## -description

Deletes the contents of a given range.

## -parameters

### -param pRange [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>*</b>

The range to delete.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Range is not degenerate.

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

## -remarks

If the text selected by the range is not completely contained by the string, the method fails.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextstrings">ITextStrings</a>