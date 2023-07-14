---
UID: NN:tuner.IDVBSLocator2
title: IDVBSLocator2 (tuner.h)
description: Provides information to enable a tuner to acquire a Digital Video Broadcasting-Satellite (DVB-S) transmission.
helpviewer_keywords: ["IDVBSLocator2","IDVBSLocator2 interface [Microsoft TV Technologies]","IDVBSLocator2 interface [Microsoft TV Technologies]","described","mstv.idvbslocator2","tuner/IDVBSLocator2"]
old-location: mstv\idvbslocator2.htm
tech.root: mstv
ms.assetid: 2f17c9a3-6ae8-4102-aee6-b2cb206d4952
ms.date: 12/05/2018
ms.keywords: IDVBSLocator2, IDVBSLocator2 interface [Microsoft TV Technologies], IDVBSLocator2 interface [Microsoft TV Technologies],described, mstv.idvbslocator2, tuner/IDVBSLocator2
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IDVBSLocator2
 - tuner/IDVBSLocator2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDVBSLocator2
---

# IDVBSLocator2 interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Provides information to enable a tuner to acquire a Digital Video Broadcasting-Satellite  (DVB-S) transmission. This interface extends the capabilities in the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator</a> interface to support the DVB-S, Second Generation (DVB-S2) specification, the Digital Satellite Equipment Control (DiSEqC) protocol, and low-noise block converters (LNBs).

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBSLocator2)</code>.