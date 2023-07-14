---
UID: NF:tuner.IDVBSLocator.get_OrbitalPosition
title: IDVBSLocator::get_OrbitalPosition (tuner.h)
description: The get_OrbitalPosition method retrieves the setting for the satellite's orbital position.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","get_OrbitalPosition method","IDVBSLocator.get_OrbitalPosition","IDVBSLocator::get_OrbitalPosition","IDVBSLocatorget_OrbitalPosition","get_OrbitalPosition","get_OrbitalPosition method [Microsoft TV Technologies]","get_OrbitalPosition method [Microsoft TV Technologies]","IDVBSLocator interface","mstv.idvbslocator_get_orbitalposition","tuner/IDVBSLocator::get_OrbitalPosition"]
old-location: mstv\idvbslocator_get_orbitalposition.htm
tech.root: mstv
ms.assetid: 3069cf27-32db-4d3f-9e61-9eddc266b540
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_OrbitalPosition method, IDVBSLocator.get_OrbitalPosition, IDVBSLocator::get_OrbitalPosition, IDVBSLocatorget_OrbitalPosition, get_OrbitalPosition, get_OrbitalPosition method [Microsoft TV Technologies], get_OrbitalPosition method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_orbitalposition, tuner/IDVBSLocator::get_OrbitalPosition
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
 - IDVBSLocator::get_OrbitalPosition
 - tuner/IDVBSLocator::get_OrbitalPosition
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
 - IDVBSLocator.get_OrbitalPosition
---

# IDVBSLocator::get_OrbitalPosition


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OrbitalPosition</b> method retrieves the setting for the satellite's orbital position.

## -parameters

### -param longitude [out]

Receives the longitude setting in tenths of a degree.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>