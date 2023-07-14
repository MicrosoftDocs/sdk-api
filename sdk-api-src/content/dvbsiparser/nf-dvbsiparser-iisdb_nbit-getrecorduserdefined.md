---
UID: NF:dvbsiparser.IISDB_NBIT.GetRecordUserDefined
title: IISDB_NBIT::GetRecordUserDefined (dvbsiparser.h)
description: Gets the user_defined field from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["GetRecordUserDefined","GetRecordUserDefined method [Microsoft TV Technologies]","GetRecordUserDefined method [Microsoft TV Technologies]","IISDB_NBIT interface","IISDB_NBIT interface [Microsoft TV Technologies]","GetRecordUserDefined method","IISDB_NBIT.GetRecordUserDefined","IISDB_NBIT::GetRecordUserDefined","dvbsiparser/IISDB_NBIT::GetRecordUserDefined","mstv.iisdb_nbit_getrecorduserdefined"]
old-location: mstv\iisdb_nbit_getrecorduserdefined.htm
tech.root: mstv
ms.assetid: 36786614-7b7e-4d76-9610-c969ad68f9d8
ms.date: 12/05/2018
ms.keywords: GetRecordUserDefined, GetRecordUserDefined method [Microsoft TV Technologies], GetRecordUserDefined method [Microsoft TV Technologies],IISDB_NBIT interface, IISDB_NBIT interface [Microsoft TV Technologies],GetRecordUserDefined method, IISDB_NBIT.GetRecordUserDefined, IISDB_NBIT::GetRecordUserDefined, dvbsiparser/IISDB_NBIT::GetRecordUserDefined, mstv.iisdb_nbit_getrecorduserdefined
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
 - IISDB_NBIT::GetRecordUserDefined
 - dvbsiparser/IISDB_NBIT::GetRecordUserDefined
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
 - IISDB_NBIT.GetRecordUserDefined
---

# IISDB_NBIT::GetRecordUserDefined


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the user_defined field from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).

## -parameters

### -param dwRecordIndex [in]

Record containing the user-defined field, indexed from zero.
Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords </a> method to get the number of records in the NBIT.

### -param pbVal [out]

Receives the user_defined field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">IISDB_NBIT::GetCountOfRecords </a>