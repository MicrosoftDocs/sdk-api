---
UID: NF:tuner.IDVBSLocator.put_OrbitalPosition
title: IDVBSLocator::put_OrbitalPosition (tuner.h)
description: The put_OrbitalPosition method sets the setting for the satellite's orbital position.
helpviewer_keywords: ["IDVBSLocator interface [Microsoft TV Technologies]","put_OrbitalPosition method","IDVBSLocator.put_OrbitalPosition","IDVBSLocator::put_OrbitalPosition","IDVBSLocatorput_OrbitalPosition","mstv.idvbslocator_put_orbitalposition","put_OrbitalPosition","put_OrbitalPosition method [Microsoft TV Technologies]","put_OrbitalPosition method [Microsoft TV Technologies]","IDVBSLocator interface","tuner/IDVBSLocator::put_OrbitalPosition"]
old-location: mstv\idvbslocator_put_orbitalposition.htm
tech.root: mstv
ms.assetid: 2de4d67c-5d99-47c2-99bf-e4f40c6247a5
ms.date: 12/05/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],put_OrbitalPosition method, IDVBSLocator.put_OrbitalPosition, IDVBSLocator::put_OrbitalPosition, IDVBSLocatorput_OrbitalPosition, mstv.idvbslocator_put_orbitalposition, put_OrbitalPosition, put_OrbitalPosition method [Microsoft TV Technologies], put_OrbitalPosition method [Microsoft TV Technologies],IDVBSLocator interface, tuner/IDVBSLocator::put_OrbitalPosition
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
 - IDVBSLocator::put_OrbitalPosition
 - tuner/IDVBSLocator::put_OrbitalPosition
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
 - IDVBSLocator.put_OrbitalPosition
---

# IDVBSLocator::put_OrbitalPosition


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_OrbitalPosition</b> method sets the setting for the satellite's orbital position.

## -parameters

### -param longitude [in]

The satellite's longitude in tenths of a degree.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbslocator">IDVBSLocator Interface</a>