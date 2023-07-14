---
UID: NF:dvbsiparser.IISDB_CDT.GetDownloadDataId
title: IISDB_CDT::GetDownloadDataId (dvbsiparser.h)
description: Receives the download_data_id field value for a logo transmission descriptor from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT). The download_data_id field identifies the data to be downloaded.
helpviewer_keywords: ["GetDownloadDataId","GetDownloadDataId method [Microsoft TV Technologies]","GetDownloadDataId method [Microsoft TV Technologies]","IISDB_CDT interface","IISDB_CDT interface [Microsoft TV Technologies]","GetDownloadDataId method","IISDB_CDT.GetDownloadDataId","IISDB_CDT::GetDownloadDataId","dvbsiparser/IISDB_CDT::GetDownloadDataId","mstv.iisdb_cdt_getdownloaddataid"]
old-location: mstv\iisdb_cdt_getdownloaddataid.htm
tech.root: mstv
ms.assetid: 87cd757e-ed10-4ad2-a9d5-4a92b8d48cd2
ms.date: 12/05/2018
ms.keywords: GetDownloadDataId, GetDownloadDataId method [Microsoft TV Technologies], GetDownloadDataId method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetDownloadDataId method, IISDB_CDT.GetDownloadDataId, IISDB_CDT::GetDownloadDataId, dvbsiparser/IISDB_CDT::GetDownloadDataId, mstv.iisdb_cdt_getdownloaddataid
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IISDB_CDT::GetDownloadDataId
 - dvbsiparser/IISDB_CDT::GetDownloadDataId
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
 - IISDB_CDT.GetDownloadDataId
---

# IISDB_CDT::GetDownloadDataId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Receives the download_data_id field value 
  for a logo transmission descriptor from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
  The download_data_id field identifies the data to be downloaded.

## -parameters

### -param pwVal [out]

Receives the download_data_id field value. This value is the same as the value of the table_id_extension field for the CDT containing the logo data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>