---
UID: NF:dvbsiparser.IIsdbSiParser2.GetCDT
title: IIsdbSiParser2::GetCDT (dvbsiparser.h)
description: Gets the common data table (CDT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A CDT contains data that is needed for receivers and stored in nonvolatile memory, such as company logos.
helpviewer_keywords: ["GetCDT","GetCDT method [Microsoft TV Technologies]","GetCDT method [Microsoft TV Technologies]","IIsdbSiParser2 interface","IIsdbSiParser2 interface [Microsoft TV Technologies]","GetCDT method","IIsdbSiParser2.GetCDT","IIsdbSiParser2::GetCDT","dvbsiparser/IIsdbSiParser2::GetCDT","mstv.iisdbsiparser2_getcdt"]
old-location: mstv\iisdbsiparser2_getcdt.htm
tech.root: mstv
ms.assetid: c984a340-d31b-43a5-baac-323629002aab
ms.date: 12/05/2018
ms.keywords: GetCDT, GetCDT method [Microsoft TV Technologies], GetCDT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetCDT method, IIsdbSiParser2.GetCDT, IIsdbSiParser2::GetCDT, dvbsiparser/IIsdbSiParser2::GetCDT, mstv.iisdbsiparser2_getcdt
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbSiParser2::GetCDT
 - dvbsiparser/IIsdbSiParser2::GetCDT
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
 - IIsdbSiParser2.GetCDT
---

# IIsdbSiParser2::GetCDT


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the common data table (CDT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A CDT contains data that is needed for receivers and stored in
  nonvolatile memory, such as company logos.

## -parameters

### -param tableId [in]

Table identifier for the type of table to retrieve. For a CDT, this value is 0xC8.

### -param bSectionNumber [in]

Specifies the value of the section_number field for the CDT.

### -param pwDownloadDataId

Pointer to the download_data_id field value for the CDT.

### -param ppCDT [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a> interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparser2">IIsdbSiParser2</a>