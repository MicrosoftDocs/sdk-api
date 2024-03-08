---
UID: NN:tvratings.IXDSToRat
title: IXDSToRat (tvratings.h)
description: The IXDSToRat interface parses rating information from extended data services (XDS) information in line 21.
helpviewer_keywords: ["IXDSToRat","IXDSToRat interface [Microsoft TV Technologies]","IXDSToRat interface [Microsoft TV Technologies]","described","IXDSToRatInterface","mstv.ixdstorat","tvratings/IXDSToRat"]
old-location: mstv\ixdstorat.htm
tech.root: mstv
ms.assetid: de65e5cd-3f4b-4925-a6b8-636fc2e332ec
ms.date: 12/05/2018
ms.keywords: IXDSToRat, IXDSToRat interface [Microsoft TV Technologies], IXDSToRat interface [Microsoft TV Technologies],described, IXDSToRatInterface, mstv.ixdstorat, tvratings/IXDSToRat
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
 - IXDSToRat
 - tvratings/IXDSToRat
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
 - IXDSToRat
---

# IXDSToRat interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IXDSToRat</b> interface parses rating information from extended data services (XDS) information in line 21. This interface is exposed by the <a href="/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> (ratings decoder) object. The XDSToRat object is implemented by third parties.

The XDS Codec filter uses this interface. Applications do not use this interface.

## -inheritance

The <b>IXDSToRat</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IXDSToRat</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IXDSToRat)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
