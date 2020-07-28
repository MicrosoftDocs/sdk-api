---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordInformationId
title: IISDB_NBIT::GetRecordInformationId (dvbsiparser.h)
description: an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["GetRecordInformationId","GetRecordInformationId method [Microsoft TV Technologies]","GetRecordInformationId method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetRecordInformationId method","IISDB_NBIT.GetRecordInformationId","IISDB_NBIT::GetRecordInformationId","dvbsiparser/IISDB_NBIT::GetRecordInformationId","mstv.iisdb_nbit_getrecordinformationid"]
old-location: mstv\iisdb_nbit_getrecordinformationid.htm
tech.root: mstv
ms.assetid: 9535d587-3e37-4d12-9b96-66ff1c2cf6f3
ms.date: 12/05/2018
ms.keywords: GetRecordInformationId, GetRecordInformationId method [Microsoft TV Technologies], GetRecordInformationId method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordInformationId method, IISDB_NBIT.GetRecordInformationId, IISDB_NBIT::GetRecordInformationId, dvbsiparser/IISDB_NBIT::GetRecordInformationId, mstv.iisdb_nbit_getrecordinformationid
f1_keywords:
- dvbsiparser/IISDB_NBIT.GetRecordInformationId
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
- IISDB_NBIT.GetRecordInformationId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_NBIT::GetRecordInformationId


## -description


an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
  


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero.
    Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a> method to get the number
    of records in the NBIT.
  


### -param pwVal [out]

Receives the information_type field for the record.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>
 

 

