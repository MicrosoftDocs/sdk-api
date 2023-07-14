---
UID: NF:tuner.IDVBSLocator.put_Azimuth
title: IDVBSLocator::put_Azimuth (tuner.h)
description: The put_Azimuth method adjusts the azimuth setting used for positioning the satellite dish.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","put_Azimuth method","IDVBSLocator.put_Azimuth","IDVBSLocator::put_Azimuth","IDVBSLocatorput_Azimuth","mstv.idvbslocator_put_azimuth","put_Azimuth","put_Azimuth method [Microsoft TV Technologies]","put_Azimuth method [Microsoft TV Technologies]","IDVBSLocator interface","tuner/IDVBSLocator::put_Azimuth"]
old-location: mstv\idvbslocator_put_azimuth.htm
tech.root: mstv
ms.assetid: 4923fa80-77f7-4d2e-9a15-ce7608888e02
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],put_Azimuth method, IDVBSLocator.put_Azimuth, IDVBSLocator::put_Azimuth, IDVBSLocatorput_Azimuth, mstv.idvbslocator_put_azimuth, put_Azimuth, put_Azimuth method [Microsoft TV Technologies], put_Azimuth method [Microsoft TV Technologies],IDVBSLocator interface, tuner/IDVBSLocator::put_Azimuth
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
 - IDVBSLocator::put_Azimuth
 - tuner/IDVBSLocator::put_Azimuth
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
 - IDVBSLocator.put_Azimuth
---

# IDVBSLocator::put_Azimuth


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Azimuth</b> method adjusts the azimuth setting used for positioning the satellite dish.

## -parameters

### -param Azimuth [in]

The azimuth, in tenths of a degree.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>