---
UID: NF:dvbsiparser.IPBDA_EIT.GetServiceIdx
title: IPBDA_EIT::GetServiceIdx (dvbsiparser.h)

description: Gets the service identifier from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream. The service identifier identifies the service that contains the events.
old-location: mstv\ipbda_eit_getserviceidx.htm
tech.root: mstv
ms.assetid: 10e8def6-be78-4b0f-8b47-d0485a1b50f1

ms.date: 12/05/2018
ms.keywords: GetServiceIdx, GetServiceIdx method [Microsoft TV Technologies], GetServiceIdx method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetServiceIdx method, IPBDA_EIT.GetServiceIdx, IPBDA_EIT::GetServiceIdx, dvbsiparser/IPBDA_EIT::GetServiceIdx, mstv.ipbda_eit_getserviceidx
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IPBDA_EIT.GetServiceIdx"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_EIT.GetServiceIdx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDA_EIT::GetServiceIdx


## -description


Gets the service identifier from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream. The service identifier identifies the service that contains the events.


## -parameters




### -param plwVal [out]

Receives the service identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>
 

 

