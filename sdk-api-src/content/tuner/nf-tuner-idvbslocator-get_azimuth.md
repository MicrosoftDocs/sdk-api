---
UID: NF:tuner.IDVBSLocator.get_Azimuth
title: IDVBSLocator::get_Azimuth (tuner.h)
description: The get_Azimuth method retrieves the azimuth setting used for positioning the satellite dish.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","get_Azimuth method","IDVBSLocator.get_Azimuth","IDVBSLocator::get_Azimuth","IDVBSLocatorget_Azimuth","get_Azimuth","get_Azimuth method [Microsoft TV Technologies]","get_Azimuth method [Microsoft TV Technologies]","IDVBSLocator interface","mstv.idvbslocator_get_azimuth","tuner/IDVBSLocator::get_Azimuth"]
old-location: mstv\idvbslocator_get_azimuth.htm
tech.root: mstv
ms.assetid: 2c1314f4-6291-4440-8010-247f8fa82d0c
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_Azimuth method, IDVBSLocator.get_Azimuth, IDVBSLocator::get_Azimuth, IDVBSLocatorget_Azimuth, get_Azimuth, get_Azimuth method [Microsoft TV Technologies], get_Azimuth method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_azimuth, tuner/IDVBSLocator::get_Azimuth
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
 - IDVBSLocator::get_Azimuth
 - tuner/IDVBSLocator::get_Azimuth
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
 - IDVBSLocator.get_Azimuth
---

# IDVBSLocator::get_Azimuth


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Azimuth</b> method retrieves the azimuth setting used for positioning the satellite dish.

## -parameters

### -param Azimuth [out]

Receives the azimuth in tenths of a degree.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>