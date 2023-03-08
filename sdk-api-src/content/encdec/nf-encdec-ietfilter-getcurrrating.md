---
UID: NF:encdec.IETFilter.GetCurrRating
title: IETFilter::GetCurrRating (encdec.h)
description: The GetCurrRating method retrieves the current rating, based on the most recent media sample.
helpviewer_keywords: ["GetCurrRating","GetCurrRating method [Microsoft TV Technologies]","GetCurrRating method [Microsoft TV Technologies]","IETFilter interface","IETFilter interface [Microsoft TV Technologies]","GetCurrRating method","IETFilter.GetCurrRating","IETFilter::GetCurrRating","IETFilterGetCurrRating","encdec/IETFilter::GetCurrRating","mstv.ietfilter_getcurrrating"]
old-location: mstv\ietfilter_getcurrrating.htm
tech.root: mstv
ms.assetid: d90d0842-2dd3-4b98-b619-1b71f7870be8
ms.date: 12/05/2018
ms.keywords: GetCurrRating, GetCurrRating method [Microsoft TV Technologies], GetCurrRating method [Microsoft TV Technologies],IETFilter interface, IETFilter interface [Microsoft TV Technologies],GetCurrRating method, IETFilter.GetCurrRating, IETFilter::GetCurrRating, IETFilterGetCurrRating, encdec/IETFilter::GetCurrRating, mstv.ietfilter_getcurrrating
req.header: encdec.h
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
 - IETFilter::GetCurrRating
 - encdec/IETFilter::GetCurrRating
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IETFilter.GetCurrRating
---

# IETFilter::GetCurrRating


## -description

The <b>GetCurrRating</b> method retrieves the current rating, based on the most recent media sample.

## -parameters

### -param pEnSystem [out]

Receives the rating system, as an <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration type.

### -param pEnRating [out]

Receives the rating level, as an <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.

### -param plbfEnAttr [out]

Receives a bitwise combination of flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration. The flags specify content attributes, such as violence or adult language. Content attributes do not apply to all rating systems.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ietfilter">IETFilter Interface</a>