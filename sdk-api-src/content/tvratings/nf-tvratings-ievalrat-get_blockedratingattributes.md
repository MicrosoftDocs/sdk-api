---
UID: NF:tvratings.IEvalRat.get_BlockedRatingAttributes
title: IEvalRat::get_BlockedRatingAttributes (tvratings.h)
description: The get_BlockedRatingAttributes method determines whether content is blocked for a given rating system and rating level.
helpviewer_keywords: ["IEvalRat interface [Microsoft TV Technologies]","get_BlockedRatingAttributes method","IEvalRat.get_BlockedRatingAttributes","IEvalRat::get_BlockedRatingAttributes","IEvalRatget_BlockedRatingAttributes","get_BlockedRatingAttributes","get_BlockedRatingAttributes method [Microsoft TV Technologies]","get_BlockedRatingAttributes method [Microsoft TV Technologies]","IEvalRat interface","mstv.ievalrat_get_blockedratingattributes","tvratings/IEvalRat::get_BlockedRatingAttributes"]
old-location: mstv\ievalrat_get_blockedratingattributes.htm
tech.root: mstv
ms.assetid: d07b6462-958c-4e97-9be1-41941aa6b747
ms.date: 12/05/2018
ms.keywords: IEvalRat interface [Microsoft TV Technologies],get_BlockedRatingAttributes method, IEvalRat.get_BlockedRatingAttributes, IEvalRat::get_BlockedRatingAttributes, IEvalRatget_BlockedRatingAttributes, get_BlockedRatingAttributes, get_BlockedRatingAttributes method [Microsoft TV Technologies], get_BlockedRatingAttributes method [Microsoft TV Technologies],IEvalRat interface, mstv.ievalrat_get_blockedratingattributes, tvratings/IEvalRat::get_BlockedRatingAttributes
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEvalRat::get_BlockedRatingAttributes
 - tvratings/IEvalRat::get_BlockedRatingAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tvratings.h
api_name:
 - IEvalRat.get_BlockedRatingAttributes
---

# IEvalRat::get_BlockedRatingAttributes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_BlockedRatingAttributes</b> method determines whether content is blocked for a given rating system and rating level.

## -parameters

### -param enSystem [in]

Specifies the rating system, as an <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration type.

### -param enLevel [in]

Specifies the rating level, as an <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.

### -param plbfAttrs [out, retval]

[out, retval] Receives a bitwise combination of flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration. The flags indicate whether the overall rating is blocked, or specific attributes within the rating are blocked.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

If the <b>BfIsBlocked</b> flag is set, all content with the specified rating level will be blocked. If one of the <b>BfIsAttr_X</b> flags is set, any content with that rating level and attribute will be blocked.

## -see-also

<a href="/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ievalrat">IEvalRat Interface</a>



<a href="/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-put_blockedratingattributes">IEvalRat::put_BlockedRatingAttributes</a>