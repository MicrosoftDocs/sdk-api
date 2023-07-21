---
UID: NF:dvbsiparser.IISDB_LDT.GetVersionHash
title: IISDB_LDT::GetVersionHash (dvbsiparser.h)
description: Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
helpviewer_keywords: ["GetVersionHash","GetVersionHash method [Microsoft TV Technologies]","GetVersionHash method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetVersionHash method","IISDB_LDT.GetVersionHash","IISDB_LDT::GetVersionHash","dvbsiparser/IISDB_LDT::GetVersionHash","mstv.iisdb_ldt_getversionhash"]
old-location: mstv\iisdb_ldt_getversionhash.htm
tech.root: mstv
ms.assetid: ea7f027c-60c3-4dcd-963b-37ae6b088c81
ms.date: 12/05/2018
ms.keywords: GetVersionHash, GetVersionHash method [Microsoft TV Technologies], GetVersionHash method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetVersionHash method, IISDB_LDT.GetVersionHash, IISDB_LDT::GetVersionHash, dvbsiparser/IISDB_LDT::GetVersionHash, mstv.iisdb_ldt_getversionhash
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
 - IISDB_LDT::GetVersionHash
 - dvbsiparser/IISDB_LDT::GetVersionHash
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
 - IISDB_LDT.GetVersionHash
---

# IISDB_LDT::GetVersionHash


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns a hash value for this instance of an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT). Tables that refer to
  the same content
  will return the same hash value, even though the tables have different version_number and table_id fields. You can use this hash value to identify when
  two tables carry the same information,
  even if the tables are carried on different transport streams.

## -parameters

### -param pdwVersionHash [out]

Receives the hash value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>