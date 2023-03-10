---
UID: NF:tom.ITextRange2.GetSubrange
title: ITextRange2::GetSubrange (tom.h)
description: Retrieves a subrange in a range.
helpviewer_keywords: ["GetSubrange","GetSubrange method [Windows Controls]","GetSubrange method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetSubrange method","ITextRange2.GetSubrange","ITextRange2::GetSubrange","controls.itextrange2_getsubrange","tom/ITextRange2::GetSubrange"]
old-location: controls\itextrange2_getsubrange.htm
tech.root: Controls
ms.assetid: 64b031cf-9d32-4e36-8e13-f32a53f00abf
ms.date: 12/05/2018
ms.keywords: GetSubrange, GetSubrange method [Windows Controls], GetSubrange method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetSubrange method, ITextRange2.GetSubrange, ITextRange2::GetSubrange, controls.itextrange2_getsubrange, tom/ITextRange2::GetSubrange
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
 - ITextRange2::GetSubrange
 - tom/ITextRange2::GetSubrange
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
 - ITextRange2.GetSubrange
---

# ITextRange2::GetSubrange


## -description

Retrieves a subrange in a range.

## -parameters

### -param iSubrange [in]

Type: <b>long</b>

The subrange index.

### -param pcpFirst [out]

Type: <b>long*</b>

The character position for the start of the subrange.

### -param pcpLim [out]

Type: <b>long*</b>

The character position for the end of the subrange.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Subranges are selected as follows.<table>
<tr>
<th>iSubrange value</th>
<th>Subrange</th>
</tr>
<tr>
<td>Equals zero</td>
<td>Gets the current active subrange.</td>
</tr>
<tr>
<td>Greater than zero</td>
<td>Gets the subrange at the index specified by <i>iSubrange</i>, in the order in which the subranges were added. This requires extra calculation.</td>
</tr>
<tr>
<td>Less than zero</td>
<td>Gets the subrange at the index specified by <i>iSubrange</i>, in increasing character position order.</td>
</tr>
</table>
 



See <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getcount">ITextRange2::GetCount</a> for the count of subranges not including the active subrange.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>