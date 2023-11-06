---
UID: NF:tuner.IDVBTLocator.get_Guard
title: IDVBTLocator::get_Guard (tuner.h)
description: The get_Guard method retrieves the guard interval.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","get_Guard method","IDVBTLocator.get_Guard","IDVBTLocator::get_Guard","IDVBTLocatorget_Guard","get_Guard","get_Guard method [Microsoft TV Technologies]","get_Guard method [Microsoft TV Technologies]","IDVBTLocator interface","mstv.idvbtlocator_get_guard","tuner/IDVBTLocator::get_Guard"]
old-location: mstv\idvbtlocator_get_guard.htm
tech.root: mstv
ms.assetid: 74b56292-eb9e-4c66-9345-f348b3d21c19
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_Guard method, IDVBTLocator.get_Guard, IDVBTLocator::get_Guard, IDVBTLocatorget_Guard, get_Guard, get_Guard method [Microsoft TV Technologies], get_Guard method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_guard, tuner/IDVBTLocator::get_Guard
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
 - IDVBTLocator::get_Guard
 - tuner/IDVBTLocator::get_Guard
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
 - IDVBTLocator.get_Guard
---

# IDVBTLocator::get_Guard


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Guard</b> method retrieves the guard interval.

## -parameters

### -param GI [out]

Receives a member of the <a href="/previous-versions/windows/desktop/mstv/guardinterval">GuardInterval</a> enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>