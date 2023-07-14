---
UID: NF:dvbsiparser.IISDB_EMM.GetTableIdExtension
title: IISDB_EMM::GetTableIdExtension (dvbsiparser.h)
description: Gets a table_id_extension field identifying a subtable within an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
helpviewer_keywords: ["GetTableIdExtension","GetTableIdExtension method [Microsoft TV Technologies]","GetTableIdExtension method [Microsoft TV Technologies]","IISDB_EMM interface","IISDB_EMM interface [Microsoft TV Technologies]","GetTableIdExtension method","IISDB_EMM.GetTableIdExtension","IISDB_EMM::GetTableIdExtension","dvbsiparser/IISDB_EMM::GetTableIdExtension","mstv.iisdb_emm_gettableidextension"]
old-location: mstv\iisdb_emm_gettableidextension.htm
tech.root: mstv
ms.assetid: aa0aba5d-181b-4466-8ad1-5db541d36261
ms.date: 12/05/2018
ms.keywords: GetTableIdExtension, GetTableIdExtension method [Microsoft TV Technologies], GetTableIdExtension method [Microsoft TV Technologies],IISDB_EMM interface, IISDB_EMM interface [Microsoft TV Technologies],GetTableIdExtension method, IISDB_EMM.GetTableIdExtension, IISDB_EMM::GetTableIdExtension, dvbsiparser/IISDB_EMM::GetTableIdExtension, mstv.iisdb_emm_gettableidextension
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
 - IISDB_EMM::GetTableIdExtension
 - dvbsiparser/IISDB_EMM::GetTableIdExtension
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
 - IISDB_EMM.GetTableIdExtension
---

# IISDB_EMM::GetTableIdExtension


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a table_id_extension field identifying a subtable within an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table.

## -parameters

### -param pwVal [out]

Receives the table_id field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a>