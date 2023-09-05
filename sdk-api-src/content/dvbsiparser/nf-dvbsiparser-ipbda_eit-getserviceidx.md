---
UID: NF:dvbsiparser.IPBDA_EIT.GetServiceIdx
title: IPBDA_EIT::GetServiceIdx (dvbsiparser.h)
description: Gets the service identifier from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream. The service identifier identifies the service that contains the events.
helpviewer_keywords: ["GetServiceIdx","GetServiceIdx method [Microsoft TV Technologies]","GetServiceIdx method [Microsoft TV Technologies]","IPBDA_EIT interface","IPBDA_EIT interface [Microsoft TV Technologies]","GetServiceIdx method","IPBDA_EIT.GetServiceIdx","IPBDA_EIT::GetServiceIdx","dvbsiparser/IPBDA_EIT::GetServiceIdx","mstv.ipbda_eit_getserviceidx"]
old-location: mstv\ipbda_eit_getserviceidx.htm
tech.root: mstv
ms.assetid: 10e8def6-be78-4b0f-8b47-d0485a1b50f1
ms.date: 12/05/2018
ms.keywords: GetServiceIdx, GetServiceIdx method [Microsoft TV Technologies], GetServiceIdx method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetServiceIdx method, IPBDA_EIT.GetServiceIdx, IPBDA_EIT::GetServiceIdx, dvbsiparser/IPBDA_EIT::GetServiceIdx, mstv.ipbda_eit_getserviceidx
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IPBDA_EIT::GetServiceIdx
 - dvbsiparser/IPBDA_EIT::GetServiceIdx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_EIT.GetServiceIdx
---

# IPBDA_EIT::GetServiceIdx


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the service identifier from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream. The service identifier identifies the service that contains the events.

## -parameters

### -param plwVal [out]

Receives the service identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>