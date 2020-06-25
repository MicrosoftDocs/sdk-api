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
f1_keywords:
- dvbsiparser/IPBDA_EIT.GetCountOfRecords
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
- IPBDA_EIT.GetCountOfRecords
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDA_EIT::GetCountOfRecords


## -description


Receives the number of event records from an  event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param pdwVal [out]

Receives the number of records.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>
 

 

