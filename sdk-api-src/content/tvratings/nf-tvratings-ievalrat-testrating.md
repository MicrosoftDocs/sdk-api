---
UID: NF:tvratings.IEvalRat.TestRating
title: IEvalRat::TestRating (tvratings.h)
description: The TestRating method determines whether a program with the specified rating should be blocked.
helpviewer_keywords: ["IEvalRat interface [Microsoft TV Technologies]","TestRating method","IEvalRat.TestRating","IEvalRat::TestRating","IEvalRatTestRating","TestRating","TestRating method [Microsoft TV Technologies]","TestRating method [Microsoft TV Technologies]","IEvalRat interface","mstv.ievalrat_testrating","tvratings/IEvalRat::TestRating"]
old-location: mstv\ievalrat_testrating.htm
tech.root: mstv
ms.assetid: 26144496-200c-49b8-9f5e-23a39fea20bc
ms.date: 12/05/2018
ms.keywords: IEvalRat interface [Microsoft TV Technologies],TestRating method, IEvalRat.TestRating, IEvalRat::TestRating, IEvalRatTestRating, TestRating, TestRating method [Microsoft TV Technologies], TestRating method [Microsoft TV Technologies],IEvalRat interface, mstv.ievalrat_testrating, tvratings/IEvalRat::TestRating
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
 - IEvalRat::TestRating
 - tvratings/IEvalRat::TestRating
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
 - IEvalRat.TestRating
---

# IEvalRat::TestRating


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>TestRating</b> method determines whether a program with the specified rating should be blocked.

## -parameters

### -param enShowSystem [in]

Specifies the rating system, as an <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration type.

### -param enShowLevel [in]

Specifies the rating level, as an <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.

### -param lbfEnShowAttributes [in]

Bitwise combination of zero or more flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration. The flags specify content attributes, such as violence or adult language. Content attributes do not apply to all rating systems.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This program is restricted and should be blocked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
This program is allowed and should not be blocked.

</td>
</tr>
</table>

## -remarks

The application sets viewing permissions through the <a href="/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-put_blockedratingattributes">IEvalRat::put_BlockedRatingAttributes</a> method. Whenever the Decrypter/Detagger filter receives a new rating in a program, it calls <b>TestRating</b> to determine whether to block the program. If <b>TestRating</b> returns S_OK, the rating is restricted under the current set of viewing permissions, and the Decrypter/Tagger filter blocks the program.

<h3><a id="Implementation_Note_"></a><a id="implementation_note_"></a><a id="IMPLEMENTATION_NOTE_"></a>Implementation Note:</h3>
For each supported rating system, store a table that contains bitmasks for each level within that system. On object creation, initialize each bitmask to zero. Update the bitmasks in the <a href="/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-put_blockedratingattributes">put_BlockedRatingAttributes</a> method.

In the <b>TestRating</b> method, use the <i>enShowSystem</i> and <i>enShowLevel</i> parameters to perform a table lookup and get the corresponding bitmask. Return S_FALSE if either of the following tests are true:

<ul>
<li>The <b>BfIsBlocked</b> flag is set in the bitmask</li>
<li>Any attribute flag in <i>lbfEnShowAttributes</i> is also set in the bitmask.</li>
</ul>
Use a bitwise <b>AND</b> to test the bitmask. If neither test is true, return S_OK.

The following code shows a possible implementation. It assumes that the object stores the bitmasks in a two-dimensional array named Mask:


```cpp

if ((0 != Mask[system][level] & BfIsBlocked) || 
    (0 != Mask[system][level] & attributes))
{
    return S_FALSE; // Blocked.
}
else
{
    return S_OK; // Not blocked.
}

```

## -see-also

<a href="/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ievalrat">IEvalRat Interface</a>