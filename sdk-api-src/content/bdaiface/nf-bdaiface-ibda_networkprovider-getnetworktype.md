---
UID: NF:bdaiface.IBDA_NetworkProvider.GetNetworkType
title: IBDA_NetworkProvider::GetNetworkType (bdaiface.h)
description: The GetNetworkType method retrieves the network type.
helpviewer_keywords: ["GetNetworkType","GetNetworkType method [Microsoft TV Technologies]","GetNetworkType method [Microsoft TV Technologies]","IBDA_NetworkProvider interface","IBDA_NetworkProvider interface [Microsoft TV Technologies]","GetNetworkType method","IBDA_NetworkProvider.GetNetworkType","IBDA_NetworkProvider::GetNetworkType","IBDA_NetworkProviderGetNetworkType","bdaiface/IBDA_NetworkProvider::GetNetworkType","mstv.ibda_networkprovider_getnetworktype"]
old-location: mstv\ibda_networkprovider_getnetworktype.htm
tech.root: mstv
ms.assetid: 38d9f099-b639-41fe-b0fd-82f056622de0
ms.date: 12/05/2018
ms.keywords: GetNetworkType, GetNetworkType method [Microsoft TV Technologies], GetNetworkType method [Microsoft TV Technologies],IBDA_NetworkProvider interface, IBDA_NetworkProvider interface [Microsoft TV Technologies],GetNetworkType method, IBDA_NetworkProvider.GetNetworkType, IBDA_NetworkProvider::GetNetworkType, IBDA_NetworkProviderGetNetworkType, bdaiface/IBDA_NetworkProvider::GetNetworkType, mstv.ibda_networkprovider_getnetworktype
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
 - IBDA_NetworkProvider::GetNetworkType
 - bdaiface/IBDA_NetworkProvider::GetNetworkType
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
 - IBDA_NetworkProvider.GetNetworkType
---

# IBDA_NetworkProvider::GetNetworkType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetNetworkType</b> method retrieves the network type.

## -parameters

### -param pguidNetworkType [in, out]

Receives a GUID specifying the network type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_networkprovider">IBDA_NetworkProvider Interface</a>