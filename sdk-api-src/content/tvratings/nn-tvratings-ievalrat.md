---
UID: NN:tvratings.IEvalRat
title: IEvalRat (tvratings.h)
description: The IEvalRat interface is used to evaluate content ratings carried by a broadcast stream.
helpviewer_keywords: ["IEvalRat","IEvalRat interface [Microsoft TV Technologies]","IEvalRat interface [Microsoft TV Technologies]","described","IEvalRatInterface","mstv.ievalrat","tvratings/IEvalRat"]
old-location: mstv\ievalrat.htm
tech.root: mstv
ms.assetid: b37c7e7d-80fd-4a42-a698-c20ffb2a5052
ms.date: 12/05/2018
ms.keywords: IEvalRat, IEvalRat interface [Microsoft TV Technologies], IEvalRat interface [Microsoft TV Technologies],described, IEvalRatInterface, mstv.ievalrat, tvratings/IEvalRat
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
 - IEvalRat
 - tvratings/IEvalRat
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
 - IEvalRat
---

# IEvalRat interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IEvalRat</b> interface is used to evaluate content ratings carried by a broadcast stream. This interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/evalrat-object">EvalRat</a> (ratings evaluator) object. The EvalRat object is implemented by third parties.

The Encrypter/Tagger filter and the Decrypter/Detagger filter use this interface. Applications use the interfaces exposed by those filters, but typically do not use the <b>IEvalRat</b> interface.

## -inheritance

The <b>IEvalRat</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEvalRat</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEvalRat)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
