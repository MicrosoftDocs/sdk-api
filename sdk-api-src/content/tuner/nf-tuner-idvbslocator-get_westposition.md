---
UID: NF:tuner.IDVBSLocator.get_WestPosition
title: IDVBSLocator::get_WestPosition (tuner.h)
description: The get_WestPosition method retrieves a value indicating whether the orbital position is given in east or west longitude.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","get_WestPosition method","IDVBSLocator.get_WestPosition","IDVBSLocator::get_WestPosition","IDVBSLocatorget_WestPosition","get_WestPosition","get_WestPosition method [Microsoft TV Technologies]","get_WestPosition method [Microsoft TV Technologies]","IDVBSLocator interface","mstv.idvbslocator_get_westposition","tuner/IDVBSLocator::get_WestPosition"]
old-location: mstv\idvbslocator_get_westposition.htm
tech.root: mstv
ms.assetid: 97bb32ba-02ca-4ea4-8364-6edddbb05d8c
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_WestPosition method, IDVBSLocator.get_WestPosition, IDVBSLocator::get_WestPosition, IDVBSLocatorget_WestPosition, get_WestPosition, get_WestPosition method [Microsoft TV Technologies], get_WestPosition method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_westposition, tuner/IDVBSLocator::get_WestPosition
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IDVBSLocator::get_WestPosition
 - tuner/IDVBSLocator::get_WestPosition
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
 - IDVBSLocator.get_WestPosition
---

# IDVBSLocator::get_WestPosition


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_WestPosition</b> method retrieves a value indicating whether the orbital position is given in east or west longitude.

## -parameters

### -param WestLongitude [out]

Pointer to a variable of type <b>VARIANT_BOOL</b>; a value of true means "west longitude."

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>