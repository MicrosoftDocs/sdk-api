---
UID: NF:bdaiface.IBDA_NetworkProvider.GetTuningSpace
title: IBDA_NetworkProvider::GetTuningSpace (bdaiface.h)
description: The GetTuningSpace method retrieves the tuning space.
helpviewer_keywords: ["GetTuningSpace","GetTuningSpace method [Microsoft TV Technologies]","GetTuningSpace method [Microsoft TV Technologies]","IBDA_NetworkProvider interface","IBDA_NetworkProvider interface [Microsoft TV Technologies]","GetTuningSpace method","IBDA_NetworkProvider.GetTuningSpace","IBDA_NetworkProvider::GetTuningSpace","IBDA_NetworkProviderGetTuningSpace","bdaiface/IBDA_NetworkProvider::GetTuningSpace","mstv.ibda_networkprovider_gettuningspace"]
old-location: mstv\ibda_networkprovider_gettuningspace.htm
tech.root: mstv
ms.assetid: 3c7305a1-4a63-42a9-abc2-ae5394c3be9a
ms.date: 12/05/2018
ms.keywords: GetTuningSpace, GetTuningSpace method [Microsoft TV Technologies], GetTuningSpace method [Microsoft TV Technologies],IBDA_NetworkProvider interface, IBDA_NetworkProvider interface [Microsoft TV Technologies],GetTuningSpace method, IBDA_NetworkProvider.GetTuningSpace, IBDA_NetworkProvider::GetTuningSpace, IBDA_NetworkProviderGetTuningSpace, bdaiface/IBDA_NetworkProvider::GetTuningSpace, mstv.ibda_networkprovider_gettuningspace
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IBDA_NetworkProvider::GetTuningSpace
 - bdaiface/IBDA_NetworkProvider::GetTuningSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_NetworkProvider.GetTuningSpace
---

# IBDA_NetworkProvider::GetTuningSpace


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetTuningSpace</b> method retrieves the tuning space.

## -parameters

### -param pguidTuingSpace [in, out]

Receives a GUID specifying the tuning space.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_networkprovider">IBDA_NetworkProvider Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_networkprovider-puttuningspace">PutTuningSpace</a>