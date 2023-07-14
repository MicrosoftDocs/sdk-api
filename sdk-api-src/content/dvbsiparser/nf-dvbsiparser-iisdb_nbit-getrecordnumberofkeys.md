---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordNumberOfKeys
title: IISDB_NBIT::GetRecordNumberOfKeys (dvbsiparser.h)
description: Returns the number_of_keys field value for a section in an for an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["GetRecordNumberOfKeys","GetRecordNumberOfKeys method [Microsoft TV Technologies]","GetRecordNumberOfKeys method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetRecordNumberOfKeys method","IISDB_NBIT.GetRecordNumberOfKeys","IISDB_NBIT::GetRecordNumberOfKeys","dvbsiparser/IISDB_NBIT::GetRecordNumberOfKeys","mstv.iisdb_nbit_getrecordnumberofkeys"]
old-location: mstv\iisdb_nbit_getrecordnumberofkeys.htm
tech.root: mstv
ms.assetid: 0ce49e6c-8a85-4620-a2ca-379c3bb30d64
ms.date: 12/05/2018
ms.keywords: GetRecordNumberOfKeys, GetRecordNumberOfKeys method [Microsoft TV Technologies], GetRecordNumberOfKeys method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordNumberOfKeys method, IISDB_NBIT.GetRecordNumberOfKeys, IISDB_NBIT::GetRecordNumberOfKeys, dvbsiparser/IISDB_NBIT::GetRecordNumberOfKeys, mstv.iisdb_nbit_getrecordnumberofkeys
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
 - IISDB_NBIT::GetRecordNumberOfKeys
 - dvbsiparser/IISDB_NBIT::GetRecordNumberOfKeys
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
 - IISDB_NBIT.GetRecordNumberOfKeys
---

# IISDB_NBIT::GetRecordNumberOfKeys


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns the number_of_keys field value for a section in an
  for an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).

## -parameters

### -param dwRecordIndex [in]

Specifies the record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a> method to get the number of records in the NBIT.

### -param pbVal [out]

Receives the number_of_keys field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords</a>