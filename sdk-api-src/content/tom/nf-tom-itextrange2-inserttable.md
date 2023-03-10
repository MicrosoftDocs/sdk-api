---
UID: NF:tom.ITextRange2.InsertTable
title: ITextRange2::InsertTable (tom.h)
description: Inserts a table in a range.
helpviewer_keywords: ["ITextRange2 interface [Windows Controls]","InsertTable method","ITextRange2.InsertTable","ITextRange2::InsertTable","InsertTable","InsertTable method [Windows Controls]","InsertTable method [Windows Controls]","ITextRange2 interface","controls.itextrange2_inserttable","tom/ITextRange2::InsertTable"]
old-location: controls\itextrange2_inserttable.htm
tech.root: Controls
ms.assetid: f62cc778-8f06-43d1-985b-d233b02d3255
ms.date: 12/05/2018
ms.keywords: ITextRange2 interface [Windows Controls],InsertTable method, ITextRange2.InsertTable, ITextRange2::InsertTable, InsertTable, InsertTable method [Windows Controls], InsertTable method [Windows Controls],ITextRange2 interface, controls.itextrange2_inserttable, tom/ITextRange2::InsertTable
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
 - ITextRange2::InsertTable
 - tom/ITextRange2::InsertTable
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
 - ITextRange2.InsertTable
---

# ITextRange2::InsertTable


## -description

Inserts a table in a range.

## -parameters

### -param cCol [in]

Type: <b>long</b>

The number of columns in the table.

### -param cRow [in]

Type: <b>long</b>

The number of rows in the table.

### -param AutoFit [in]

Type: <b>long</b>

Specifies how the cells fit the target space.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -remarks

If the range is nondegenerate, the table replaces the text in the range. The column widths are calculated according to the <i>AutoFit</i> parameter, and the borders are solid black with 0.5 point widths. To change these defaults, use the <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getrow">ITextRange2::GetRow</a> method to obtain an <a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a> interface.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>