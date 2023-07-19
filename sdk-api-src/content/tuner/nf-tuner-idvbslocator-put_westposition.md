---
UID: NF:tuner.IDVBSLocator.put_WestPosition
title: IDVBSLocator::put_WestPosition (tuner.h)
description: The put_WestPosition method sets the longitudinal position as west longitude or east longitude.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","put_WestPosition method","IDVBSLocator.put_WestPosition","IDVBSLocator::put_WestPosition","IDVBSLocatorput_WestPosition","mstv.idvbslocator_put_westposition","put_WestPosition","put_WestPosition method [Microsoft TV Technologies]","put_WestPosition method [Microsoft TV Technologies]","IDVBSLocator interface","tuner/IDVBSLocator::put_WestPosition"]
old-location: mstv\idvbslocator_put_westposition.htm
tech.root: mstv
ms.assetid: 567aa90e-6179-477a-813d-13e99b16bbc2
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],put_WestPosition method, IDVBSLocator.put_WestPosition, IDVBSLocator::put_WestPosition, IDVBSLocatorput_WestPosition, mstv.idvbslocator_put_westposition, put_WestPosition, put_WestPosition method [Microsoft TV Technologies], put_WestPosition method [Microsoft TV Technologies],IDVBSLocator interface, tuner/IDVBSLocator::put_WestPosition
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
 - IDVBSLocator::put_WestPosition
 - tuner/IDVBSLocator::put_WestPosition
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
 - IDVBSLocator.put_WestPosition
---

# IDVBSLocator::put_WestPosition


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_WestPosition</b> method sets the longitudinal position as west longitude or east longitude.

## -parameters

### -param WestLongitude [in]

Specifies whether the following longitude values that follow will be west or east longitude. True means "west longitude."

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>