---
UID: NN:encdec.IDTFilter
title: IDTFilter (encdec.h)
description: The IDTFilter interface is exposed by the Decrypter/Detagger filter. Applications can use this interface to set the ratings permissions.
helpviewer_keywords: ["IDTFilter","IDTFilter interface [Microsoft TV Technologies]","IDTFilter interface [Microsoft TV Technologies]","described","IDTFilterInterface","encdec/IDTFilter","mstv.idtfilter"]
old-location: mstv\idtfilter.htm
tech.root: mstv
ms.assetid: 15acf764-7e4d-40c3-b907-ff5dfaa69dae
ms.date: 12/05/2018
ms.keywords: IDTFilter, IDTFilter interface [Microsoft TV Technologies], IDTFilter interface [Microsoft TV Technologies],described, IDTFilterInterface, encdec/IDTFilter, mstv.idtfilter
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
 - IDTFilter
 - encdec/IDTFilter
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
 - IDTFilter
---

# IDTFilter interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IDTFilter</b> interface is exposed by the Decrypter/Detagger filter. Applications can use this interface to set the ratings permissions.

## -inheritance

The <b>IDTFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDTFilter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilter)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
