---
UID: NF:tom.ITextRow.GetCellColorFore
title: ITextRow::GetCellColorFore (tom.h)
description: Gets the foreground color of the active cell.
helpviewer_keywords: ["GetCellColorFore","GetCellColorFore method [Windows Controls]","GetCellColorFore method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellColorFore method","ITextRow.GetCellColorFore","ITextRow::GetCellColorFore","controls.itextrow_getcellcolorfore","tom/ITextRow::GetCellColorFore"]
old-location: controls\itextrow_getcellcolorfore.htm
tech.root: Controls
ms.assetid: 92c8bff3-a56b-4adc-9f49-728f22c1089b
ms.date: 12/05/2018
ms.keywords: GetCellColorFore, GetCellColorFore method [Windows Controls], GetCellColorFore method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellColorFore method, ITextRow.GetCellColorFore, ITextRow::GetCellColorFore, controls.itextrow_getcellcolorfore, tom/ITextRow::GetCellColorFore
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
 - ITextRow::GetCellColorFore
 - tom/ITextRow::GetCellColorFore
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
 - ITextRow.GetCellColorFore
---

# ITextRow::GetCellColorFore


## -description

Gets the foreground color of the active cell.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The foreground color.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
</table>

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellcolorfore">ITextRow::SetCellColorFore</a>