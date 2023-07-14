---
UID: NF:dvbsiparser.IPBDA_EIT.GetCountOfRecords
title: IPBDA_EIT::GetCountOfRecords (dvbsiparser.h)
description: Receives the number of event records from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IPBDA_EIT interface","IPBDA_EIT interface [Microsoft TV Technologies]","GetCountOfRecords method","IPBDA_EIT.GetCountOfRecords","IPBDA_EIT::GetCountOfRecords","dvbsiparser/IPBDA_EIT::GetCountOfRecords","mstv.ipbda_eit_getcountofrecords"]
old-location: mstv\ipbda_eit_getcountofrecords.htm
tech.root: mstv
ms.assetid: 7f09421d-ae19-4c8e-93a2-31fa8697742a
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetCountOfRecords method, IPBDA_EIT.GetCountOfRecords, IPBDA_EIT::GetCountOfRecords, dvbsiparser/IPBDA_EIT::GetCountOfRecords, mstv.ipbda_eit_getcountofrecords
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
 - IPBDA_EIT::GetCountOfRecords
 - dvbsiparser/IPBDA_EIT::GetCountOfRecords
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
 - IPBDA_EIT.GetCountOfRecords
---

# IPBDA_EIT::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Receives the number of event records from an  event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param pdwVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>