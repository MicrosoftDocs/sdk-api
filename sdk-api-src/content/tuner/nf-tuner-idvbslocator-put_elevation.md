---
UID: NF:tuner.IDVBSLocator.put_Elevation
title: IDVBSLocator::put_Elevation (tuner.h)
description: The put_Elevation method sets the elevation of the satellite in tenths of a degree.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","put_Elevation method","IDVBSLocator.put_Elevation","IDVBSLocator::put_Elevation","IDVBSLocatorput_Elevation","mstv.idvbslocator_put_elevation","put_Elevation","put_Elevation method [Microsoft TV Technologies]","put_Elevation method [Microsoft TV Technologies]","IDVBSLocator interface","tuner/IDVBSLocator::put_Elevation"]
old-location: mstv\idvbslocator_put_elevation.htm
tech.root: mstv
ms.assetid: 12db3e20-9102-483c-a4ef-8a90a376b7af
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],put_Elevation method, IDVBSLocator.put_Elevation, IDVBSLocator::put_Elevation, IDVBSLocatorput_Elevation, mstv.idvbslocator_put_elevation, put_Elevation, put_Elevation method [Microsoft TV Technologies], put_Elevation method [Microsoft TV Technologies],IDVBSLocator interface, tuner/IDVBSLocator::put_Elevation
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
 - IDVBSLocator::put_Elevation
 - tuner/IDVBSLocator::put_Elevation
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
 - IDVBSLocator.put_Elevation
---

# IDVBSLocator::put_Elevation


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Elevation</b> method sets the elevation of the satellite in tenths of a degree.

## -parameters

### -param Elevation [in]

The elevation, in tenths of a degree.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>