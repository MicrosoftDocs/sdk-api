---
UID: NF:textstor.ITextStoreACP2.GetACPFromPoint
title: ITextStoreACP2::GetACPFromPoint (textstor.h)
description: Converts a point in screen coordinates to an application character position.
helpviewer_keywords: ["GXFPF_NEAREST","GXFPF_ROUND_NEAREST","GetACPFromPoint","GetACPFromPoint method [Text Services Framework]","GetACPFromPoint method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","GetACPFromPoint method","ITextStoreACP2.GetACPFromPoint","ITextStoreACP2::GetACPFromPoint","textstor/ITextStoreACP2::GetACPFromPoint","tsf.itextstoreacp2_getacpfrompoint"]
old-location: tsf\itextstoreacp2_getacpfrompoint.htm
tech.root: TSF
ms.assetid: 2907cd34-6ebe-45b4-afd6-8062212c3dc9
ms.date: 12/05/2018
ms.keywords: GXFPF_NEAREST, GXFPF_ROUND_NEAREST, GetACPFromPoint, GetACPFromPoint method [Text Services Framework], GetACPFromPoint method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetACPFromPoint method, ITextStoreACP2.GetACPFromPoint, ITextStoreACP2::GetACPFromPoint, textstor/ITextStoreACP2::GetACPFromPoint, tsf.itextstoreacp2_getacpfrompoint
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::GetACPFromPoint
 - textstor/ITextStoreACP2::GetACPFromPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.GetACPFromPoint
---

# ITextStoreACP2::GetACPFromPoint


## -description

Converts a point in screen coordinates to an application character position.

## -parameters

### -param vcView [in]

Specifies the context view.

### -param ptScreen [in]

Pointer to the <b>POINT</b> structure with the screen coordinates of the point.

### -param dwFlags [in]

Specifies the character position to return based upon the screen coordinates of the point relative to a character bounding box. By default, the character position returned is the character bounding box containing the screen coordinates of the point. If the point is outside a character bounding box, the method returns <b>NULL</b> or <a href="/windows/desktop/TSF/manager-return-values">TF_E_INVALIDPOINT</a>. Other bit flags for this parameter are as follows.

The bit flags can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GXFPF_ROUND_NEAREST"></a><a id="gxfpf_round_nearest"></a><dl>
<dt><b>GXFPF_ROUND_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.

</td>
</tr>
<tr>
<td width="40%"><a id="GXFPF_NEAREST"></a><a id="gxfpf_nearest"></a><dl>
<dt><b>GXFPF_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.

</td>
</tr>
</table>

### -param pacp [out]

Receives the character position that corresponds to the screen coordinates of the point.

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
<dt><b>TS_E_INVALIDPOINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>ptScreen</i> parameter is not within the bounding box of any character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/TSF/gxfpf--constants">GXFPF_* Constants
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getacpfrompoint">ITfContextOwner::GetACPFromPoint
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-getrangefrompoint">ITfContextView::GetRangeFromPoint
      </a>



<a href="/windows/desktop/TSF/manager-return-values">Manager Return Values
      </a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>