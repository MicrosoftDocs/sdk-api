---
UID: NF:tuner.IDVBSLocator.get_Elevation
title: IDVBSLocator::get_Elevation (tuner.h)
description: The get_Elevation method retrieves the elevation of the satellite in tenths of a degree.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","get_Elevation method","IDVBSLocator.get_Elevation","IDVBSLocator::get_Elevation","IDVBSLocatorget_Elevation","get_Elevation","get_Elevation method [Microsoft TV Technologies]","get_Elevation method [Microsoft TV Technologies]","IDVBSLocator interface","mstv.idvbslocator_get_elevation","tuner/IDVBSLocator::get_Elevation"]
old-location: mstv\idvbslocator_get_elevation.htm
tech.root: mstv
ms.assetid: 8d81cb6d-412f-4a55-b9fc-a0a0e8cebaaa
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_Elevation method, IDVBSLocator.get_Elevation, IDVBSLocator::get_Elevation, IDVBSLocatorget_Elevation, get_Elevation, get_Elevation method [Microsoft TV Technologies], get_Elevation method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_elevation, tuner/IDVBSLocator::get_Elevation
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
 - IDVBSLocator::get_Elevation
 - tuner/IDVBSLocator::get_Elevation
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
 - IDVBSLocator.get_Elevation
---

# IDVBSLocator::get_Elevation


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Elevation</b> method retrieves the elevation of the satellite in tenths of a degree.

## -parameters

### -param Elevation [out]

Receives the elevation setting in tenths of a degree.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>