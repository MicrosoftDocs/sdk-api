---
UID: NF:tvratings.IEvalRat.put_BlockedRatingAttributes
title: IEvalRat::put_BlockedRatingAttributes (tvratings.h)
description: The put_BlockedRatingAttributes method specifies whether to block content that has a specified rating.
helpviewer_keywords: ["IEvalRat interface [Microsoft TV Technologies]","put_BlockedRatingAttributes method","IEvalRat.put_BlockedRatingAttributes","IEvalRat::put_BlockedRatingAttributes","IEvalRatput_BlockedRatingAttributes","mstv.ievalrat_put_blockedratingattributes","put_BlockedRatingAttributes","put_BlockedRatingAttributes method [Microsoft TV Technologies]","put_BlockedRatingAttributes method [Microsoft TV Technologies]","IEvalRat interface","tvratings/IEvalRat::put_BlockedRatingAttributes"]
old-location: mstv\ievalrat_put_blockedratingattributes.htm
tech.root: mstv
ms.assetid: 7c6919f0-1270-4dcd-8180-a9af4763c580
ms.date: 12/05/2018
ms.keywords: IEvalRat interface [Microsoft TV Technologies],put_BlockedRatingAttributes method, IEvalRat.put_BlockedRatingAttributes, IEvalRat::put_BlockedRatingAttributes, IEvalRatput_BlockedRatingAttributes, mstv.ievalrat_put_blockedratingattributes, put_BlockedRatingAttributes, put_BlockedRatingAttributes method [Microsoft TV Technologies], put_BlockedRatingAttributes method [Microsoft TV Technologies],IEvalRat interface, tvratings/IEvalRat::put_BlockedRatingAttributes
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
 - IEvalRat::put_BlockedRatingAttributes
 - tvratings/IEvalRat::put_BlockedRatingAttributes
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
 - IEvalRat.put_BlockedRatingAttributes
---

# IEvalRat::put_BlockedRatingAttributes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_BlockedRatingAttributes</b> method specifies whether to block content that has a specified rating.

## -parameters

### -param enSystem [in]

Specifies the rating system, as an <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration type.

### -param enLevel [in]

Specifies the rating level, as an <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.

### -param lbfAttrs [in]

Bitwise combination of zero or more flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration. The flags specify whether the overall rating is blocked, or specific attributes within the rating are blocked.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method should be called once for each level in a rating system, to specify viewing permissions for that level. The <i>lbfAttrs</i> parameter indicates the permissions for the specified rating level:

<ul>
<li>If no flags are set, this rating level is unrestricted. Any program with this rating level can be viewed.</li>
<li>If the <b>BflsBlocked</b> flag is set, this rating level is restricted. No program with this rating level can be viewed.</li>
<li>Flags in the range <b>BfIsAttr_1</b> to <b>BfIsAttr_7</b> specify content attributes, such as violence or adult language. If one of these flags is set, it means that a program with that content attribute and the specified rating level will be blocked.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ievalrat">IEvalRat Interface</a>