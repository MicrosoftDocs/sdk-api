---
UID: NF:tom.ITextPara2.SetDuplicate2
title: ITextPara2::SetDuplicate2 (tom.h)
description: Sets the properties of this object by copying the properties of another text paragraph object.
helpviewer_keywords: ["ITextPara2 interface [Windows Controls]","SetDuplicate2 method","ITextPara2.SetDuplicate2","ITextPara2::SetDuplicate2","SetDuplicate2","SetDuplicate2 method [Windows Controls]","SetDuplicate2 method [Windows Controls]","ITextPara2 interface","controls.itextpara2_setduplicate2","tom/ITextPara2::SetDuplicate2"]
old-location: controls\itextpara2_setduplicate2.htm
tech.root: Controls
ms.assetid: 403fd23b-5d66-4e30-b1aa-eec9e4676318
ms.date: 12/05/2018
ms.keywords: ITextPara2 interface [Windows Controls],SetDuplicate2 method, ITextPara2.SetDuplicate2, ITextPara2::SetDuplicate2, SetDuplicate2, SetDuplicate2 method [Windows Controls], SetDuplicate2 method [Windows Controls],ITextPara2 interface, controls.itextpara2_setduplicate2, tom/ITextPara2::SetDuplicate2
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
 - ITextPara2::SetDuplicate2
 - tom/ITextPara2::SetDuplicate2
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
 - ITextPara2.SetDuplicate2
---

# ITextPara2::SetDuplicate2


## -description

Sets the properties of this object by copying the properties of another text paragraph object.

## -parameters

### -param pPara [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>*</b>

The text paragraph object to copy from.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara2::SetDuplicate2</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

## -remarks

<b>tomUndefined</b> values have no effect.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara2-getduplicate2">ITextPara2::GetDuplicate2</a>