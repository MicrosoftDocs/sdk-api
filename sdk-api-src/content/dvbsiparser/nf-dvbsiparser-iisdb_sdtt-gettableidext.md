---
UID: NF:dvbsiparser.IISDB_SDTT.GetTableIdExt
title: IISDB_SDTT::GetTableIdExt (dvbsiparser.h)
description: Gets the table_id_extension field value from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT). This field value identifies a specific instance of an SDTT.
helpviewer_keywords: ["GetTableIdExt","GetTableIdExt method [Microsoft TV Technologies]","GetTableIdExt method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetTableIdExt method","IISDB_SDTT.GetTableIdExt","IISDB_SDTT::GetTableIdExt","dvbsiparser/IISDB_SDTT::GetTableIdExt","mstv.iisdb_sdtt_gettableidext"]
old-location: mstv\iisdb_sdtt_gettableidext.htm
tech.root: mstv
ms.assetid: 2b77ce3b-c706-4820-88dc-08b37978664b
ms.date: 12/05/2018
ms.keywords: GetTableIdExt, GetTableIdExt method [Microsoft TV Technologies], GetTableIdExt method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetTableIdExt method, IISDB_SDTT.GetTableIdExt, IISDB_SDTT::GetTableIdExt, dvbsiparser/IISDB_SDTT::GetTableIdExt, mstv.iisdb_sdtt_gettableidext
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
 - IISDB_SDTT::GetTableIdExt
 - dvbsiparser/IISDB_SDTT::GetTableIdExt
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
 - IISDB_SDTT.GetTableIdExt
---

# IISDB_SDTT::GetTableIdExt


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the table_id_extension field value from
  an Integrated Services Digital Broadcasting (ISDB)  software download
  trigger table
  (SDTT). This field value identifies a specific instance of an SDTT.

## -parameters

### -param pwVal [out]

Receives the table_id_extension field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>