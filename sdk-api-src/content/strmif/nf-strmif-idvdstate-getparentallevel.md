---
UID: NF:strmif.IDvdState.GetParentalLevel
title: IDvdState::GetParentalLevel (strmif.h)
description: The GetParentalLevel method retrieves the user's parental level as saved in the DvdState object.
helpviewer_keywords: ["GetParentalLevel","GetParentalLevel method [DirectShow]","GetParentalLevel method [DirectShow]","IDvdState interface","IDvdState interface [DirectShow]","GetParentalLevel method","IDvdState.GetParentalLevel","IDvdState::GetParentalLevel","IDvdStateGetParentalLevel","dshow.idvdstate_getparentallevel","strmif/IDvdState::GetParentalLevel"]
old-location: dshow\idvdstate_getparentallevel.htm
tech.root: dshow
ms.assetid: f87c128f-d751-4593-ac26-3249b803bbe4
ms.date: 12/05/2018
ms.keywords: GetParentalLevel, GetParentalLevel method [DirectShow], GetParentalLevel method [DirectShow],IDvdState interface, IDvdState interface [DirectShow],GetParentalLevel method, IDvdState.GetParentalLevel, IDvdState::GetParentalLevel, IDvdStateGetParentalLevel, dshow.idvdstate_getparentallevel, strmif/IDvdState::GetParentalLevel
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdState::GetParentalLevel
 - strmif/IDvdState::GetParentalLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdState.GetParentalLevel
---

# IDvdState::GetParentalLevel


## -description

The <code>GetParentalLevel</code> method retrieves the user's parental level as saved in the <b>DvdState</b> object.

## -parameters

### -param pulParentalLevel [out]

Receives the parental level.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdstate">IDvdState Interface</a>