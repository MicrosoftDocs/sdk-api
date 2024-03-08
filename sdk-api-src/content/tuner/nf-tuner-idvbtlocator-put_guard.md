---
UID: NF:tuner.IDVBTLocator.put_Guard
title: IDVBTLocator::put_Guard (tuner.h)
description: The put_Guard method sets the guard interval.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","put_Guard method","IDVBTLocator.put_Guard","IDVBTLocator::put_Guard","IDVBTLocatorput_Guard","mstv.idvbtlocator_put_guard","put_Guard","put_Guard method [Microsoft TV Technologies]","put_Guard method [Microsoft TV Technologies]","IDVBTLocator interface","tuner/IDVBTLocator::put_Guard"]
old-location: mstv\idvbtlocator_put_guard.htm
tech.root: mstv
ms.assetid: af0accaf-ef33-4074-ac04-2bd09f3ad879
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_Guard method, IDVBTLocator.put_Guard, IDVBTLocator::put_Guard, IDVBTLocatorput_Guard, mstv.idvbtlocator_put_guard, put_Guard, put_Guard method [Microsoft TV Technologies], put_Guard method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_Guard
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
 - IDVBTLocator::put_Guard
 - tuner/IDVBTLocator::put_Guard
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
 - IDVBTLocator.put_Guard
---

# IDVBTLocator::put_Guard


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Guard</b> method sets the guard interval.

## -parameters

### -param GI [in]

Variable of type <a href="/previous-versions/windows/desktop/mstv/guardinterval">GuardInterval</a> that specifies the guard interval.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>