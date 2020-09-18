---
UID: NF:tom.ITextFont2.SetDuplicate2
title: ITextFont2::SetDuplicate2 (tom.h)
description: Sets the properties of this object by copying the properties of another text font object.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetDuplicate2 method","ITextFont2.SetDuplicate2","ITextFont2::SetDuplicate2","SetDuplicate2","SetDuplicate2 method [Windows Controls]","SetDuplicate2 method [Windows Controls]","ITextFont2 interface","controls.itextfont2_setduplicate2","tom/ITextFont2::SetDuplicate2"]
old-location: controls\itextfont2_setduplicate2.htm
tech.root: Controls
ms.assetid: aaaafed9-be20-40a2-beed-09703970452f
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetDuplicate2 method, ITextFont2.SetDuplicate2, ITextFont2::SetDuplicate2, SetDuplicate2, SetDuplicate2 method [Windows Controls], SetDuplicate2 method [Windows Controls],ITextFont2 interface, controls.itextfont2_setduplicate2, tom/ITextFont2::SetDuplicate2
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
 - ITextFont2::SetDuplicate2
 - tom/ITextFont2::SetDuplicate2
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
 - ITextFont2.SetDuplicate2
---

# ITextFont2::SetDuplicate2


## -description

Sets the properties of this object by copying the properties of another text font object.

## -parameters

### -param pFont [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>*</b>

The text font object to copy from.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

## -remarks

Values with the <b>tomUndefined</b> attribute have no effect.

For an example of how to use font duplicates, see <a href="/windows/desktop/api/tom/nf-tom-itextrange-setfont">ITextRange::SetFont</a>.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-getduplicate2">ITextFont2::GetDuplicate2</a>