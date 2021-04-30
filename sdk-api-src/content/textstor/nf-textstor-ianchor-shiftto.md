---
UID: NF:textstor.IAnchor.ShiftTo
title: IAnchor::ShiftTo (textstor.h)
description: The IAnchor::ShiftTo method shifts the current anchor to the same position as another anchor.
helpviewer_keywords: ["IAnchor interface [Text Services Framework]","ShiftTo method","IAnchor.ShiftTo","IAnchor::ShiftTo","ShiftTo","ShiftTo method [Text Services Framework]","ShiftTo method [Text Services Framework]","IAnchor interface","textstor/IAnchor::ShiftTo","tsf.ianchor_shiftto"]
old-location: tsf\ianchor_shiftto.htm
tech.root: TSF
ms.assetid: a0fb9a08-3f46-4d2f-8887-e80dc0bade1b
ms.date: 12/05/2018
ms.keywords: IAnchor interface [Text Services Framework],ShiftTo method, IAnchor.ShiftTo, IAnchor::ShiftTo, ShiftTo, ShiftTo method [Text Services Framework], ShiftTo method [Text Services Framework],IAnchor interface, textstor/IAnchor::ShiftTo, tsf.ianchor_shiftto
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IAnchor::ShiftTo
 - textstor/IAnchor::ShiftTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IAnchor.ShiftTo
---

# IAnchor::ShiftTo


## -description

The <b>IAnchor::ShiftTo</b> method shifts the current anchor to the same position as another anchor.

## -parameters

### -param paSite [in]

Anchor occupying a position that the current anchor will be moved to.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An <a href="/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a> interface pointer to the <i>paSite</i> anchor could not be obtained, or memory is too low to safely complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>paSite</i> is invalid.

</td>
</tr>
</table>

## -remarks

Implementing this method is usually more efficient than an equivalent <a href="/windows/desktop/api/textstor/nf-textstor-ianchor-shift">IAnchor::Shift</a> operation.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-ianchor-shift">IAnchor::Shift
      </a>