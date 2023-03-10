---
UID: NF:msctf.ITfContextOwner.GetACPFromPoint
title: ITfContextOwner::GetACPFromPoint (msctf.h)
description: The ITfContextOwner::GetACPFromPoint method converts a point in screen coordinates to an application character position.
helpviewer_keywords: ["GetACPFromPoint","GetACPFromPoint method [Text Services Framework]","GetACPFromPoint method [Text Services Framework]","ITfContextOwner interface","ITfContextOwner interface [Text Services Framework]","GetACPFromPoint method","ITfContextOwner.GetACPFromPoint","ITfContextOwner::GetACPFromPoint","_tsf_itfcontextowner_getacpfrompoint_ref","msctf/ITfContextOwner::GetACPFromPoint","tsf.itfcontextowner_getacpfrompoint"]
old-location: tsf\itfcontextowner_getacpfrompoint.htm
tech.root: TSF
ms.assetid: f8091e79-33af-49d5-b3c8-d30952c62010
ms.date: 12/05/2018
ms.keywords: GetACPFromPoint, GetACPFromPoint method [Text Services Framework], GetACPFromPoint method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetACPFromPoint method, ITfContextOwner.GetACPFromPoint, ITfContextOwner::GetACPFromPoint, _tsf_itfcontextowner_getacpfrompoint_ref, msctf/ITfContextOwner::GetACPFromPoint, tsf.itfcontextowner_getacpfrompoint
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msimtf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwner::GetACPFromPoint
 - msctf/ITfContextOwner::GetACPFromPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetACPFromPoint
---

# ITfContextOwner::GetACPFromPoint


## -description

The <b>ITfContextOwner::GetACPFromPoint</b> method converts a point in screen coordinates to an application character position.

## -parameters

### -param ptScreen [in]

Pointer to the <b>POINT</b> structure with the screen coordinates of the point.

### -param dwFlags [in]

Specifies the character position to return based upon the screen coordinates of the point relative to a character bounding box. By default, the character position returned is the character bounding box containing the screen coordinates of the point. If the point is outside a character's bounding box, the method returns <b>NULL</b> or TF_E_INVALIDPOINT.

If the GXFPF_ROUND_NEAREST flag is specified for this parameter and the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.

If the GXFPF_NEAREST flag is specified for this parameter and the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.

The bit flags can be combined.

### -param pacp [out]

Receives the character position that corresponds to the screen coordinates of the point

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

## -remarks

<img alt="Point 1 is in character bounding box and point 2 is outside the character bounding box." border="border" src="./images/ACPFig01.gif"/>
Use the illustration to determine the character position returned based on the flags used in the <i>dwFlags</i> parameter.

<b>Point 1
      </b>

<ul>
<li>Default-- <i>pacp = 0</i> --The screen coordinates of the point is inside the character bounding box of Character Position 0.</li>
<li>GXFPF_ROUND_NEAREST-- <i>pacp = 1</i> --The screen coordinates of the point is closest to Range Position 1 which is the starting range position of Character Position 1.</li>
<li>GXFPF_NEAREST-- <i>pacp = 0</i> --The default behavior occurs because the point lies within the character bounding box of Character Position 0.</li>
</ul>
<b>Point 2</b>

<ul>
<li>Default-- <i>hr = TF_E_INVALIDPOINT</i> --The screen coordinates of the point is outside a character bounding box.</li>
<li>GXFPF_ROUND_NEAREST-- <i>hr = TF_E_INVALIDPOINT</i> --The default behavior occurs because the screen coordinates of the point is outside a character bounding box.</li>
<li>GXFPF_NEAREST-- <i>pacp = 1</i> --The closest character position to the screen coordinates of the point is Character Position 1.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">ITextStoreACP::GetACPFromPoint
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextowner">ITfContextOwner</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextview-getrangefrompoint">ITfContextView::GetRangeFromPoint
      </a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>