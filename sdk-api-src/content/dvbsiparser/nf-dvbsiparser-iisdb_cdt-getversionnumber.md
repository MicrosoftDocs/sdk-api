---
UID: NF:dvbsiparser.IISDB_CDT.GetVersionNumber
title: IISDB_CDT::GetVersionNumber (dvbsiparser.h)
description: Gets the version number for an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IISDB_CDT interface","IISDB_CDT interface [Microsoft TV Technologies]","GetVersionNumber method","IISDB_CDT.GetVersionNumber","IISDB_CDT::GetVersionNumber","dvbsiparser/IISDB_CDT::GetVersionNumber","mstv.iisdb_cdt_getversionnumber"]
old-location: mstv\iisdb_cdt_getversionnumber.htm
tech.root: mstv
ms.assetid: 4c88ecdb-8e01-4fec-96f2-c67331b6d071
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetVersionNumber method, IISDB_CDT.GetVersionNumber, IISDB_CDT::GetVersionNumber, dvbsiparser/IISDB_CDT::GetVersionNumber, mstv.iisdb_cdt_getversionnumber
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
 - IISDB_CDT::GetVersionNumber
 - dvbsiparser/IISDB_CDT::GetVersionNumber
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
 - IISDB_CDT.GetVersionNumber
---

# IISDB_CDT::GetVersionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the version number for an Integrated Services Digital Broadcasting (ISDB)
  common data table (CDT).

## -parameters

### -param pbVal [out]

Receives the version_number field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>