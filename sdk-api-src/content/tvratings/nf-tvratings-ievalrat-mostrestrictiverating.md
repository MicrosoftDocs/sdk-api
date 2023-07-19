---
UID: NF:tvratings.IEvalRat.MostRestrictiveRating
title: IEvalRat::MostRestrictiveRating (tvratings.h)
description: The MostRestrictiveRating method compares two ratings and returns the more restrictive of the two.
helpviewer_keywords: ["IEvalRat interface [Microsoft TV Technologies]","MostRestrictiveRating method","IEvalRat.MostRestrictiveRating","IEvalRat::MostRestrictiveRating","IEvalRatMostRestrictiveRating","MostRestrictiveRating","MostRestrictiveRating method [Microsoft TV Technologies]","MostRestrictiveRating method [Microsoft TV Technologies]","IEvalRat interface","mstv.ievalrat_mostrestrictiverating","tvratings/IEvalRat::MostRestrictiveRating"]
old-location: mstv\ievalrat_mostrestrictiverating.htm
tech.root: mstv
ms.assetid: b744715f-53a8-4011-9657-d2962f0e7f6e
ms.date: 12/05/2018
ms.keywords: IEvalRat interface [Microsoft TV Technologies],MostRestrictiveRating method, IEvalRat.MostRestrictiveRating, IEvalRat::MostRestrictiveRating, IEvalRatMostRestrictiveRating, MostRestrictiveRating, MostRestrictiveRating method [Microsoft TV Technologies], MostRestrictiveRating method [Microsoft TV Technologies],IEvalRat interface, mstv.ievalrat_mostrestrictiverating, tvratings/IEvalRat::MostRestrictiveRating
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
 - IEvalRat::MostRestrictiveRating
 - tvratings/IEvalRat::MostRestrictiveRating
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
 - IEvalRat.MostRestrictiveRating
---

# IEvalRat::MostRestrictiveRating


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>MostRestrictiveRating</b> method compares two ratings and returns the more restrictive of the two.

## -parameters

### -param enSystem1 [in]

The rating system of the first rating to compare, specified as a member of the <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration.

### -param enEnLevel1 [in]

The rating level of the first rating, specified as a member of the <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration.

### -param lbfEnAttr1 [in]

Specifies the content attributes of the first rating, as a bitwise combination of flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration.

### -param enSystem2 [in]

The rating system of the second rating to compare, specified as a member of the <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration.

### -param enEnLevel2 [in]

The rating level of the second rating, specified as a member of the <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration.

### -param lbfEnAttr2 [in]

Specifies the content attributes of the second rating, as a bitwise combination of flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration.

### -param penSystem [out]

Receives the rating system of the more restrictive rating.

### -param penEnLevel [out]

Receives the rating level of the more restrictive rating.

### -param plbfEnAttr [out]

Receives a bitwise combination of flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The ratings are from two different rating systems.

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

This method enables the client to determine which of two ratings is more restrictive. For example, in the MPAA system, PG is more restrictive than R. The more restrictive rating is returned in the <i>penSystem</i>, <i>penEnLevel</i>, and <i>plbfEnAttr</i> parameters.

When the method compares ratings from two different ratings systems, it returns a rating expressed in the first system, unless the first system is unknown (TvRat_SystemDontKnow). In that case, it returns a rating using the second system.

The method returns S_FALSE if the ratings systems are not the same. There may not be an exact mapping between the two systems.

## -see-also

<a href="/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ievalrat">IEvalRat Interface</a>