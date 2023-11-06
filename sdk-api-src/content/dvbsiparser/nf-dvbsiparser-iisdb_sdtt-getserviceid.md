---
UID: NF:dvbsiparser.IISDB_SDTT.GetServiceId
title: IISDB_SDTT::GetServiceId (dvbsiparser.h)
description: Receives the service_id field that uniquely identifies a service from an Integrated Services Digital Broadcasting System (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetServiceId","GetServiceId method [Microsoft TV Technologies]","GetServiceId method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetServiceId method","IISDB_SDTT.GetServiceId","IISDB_SDTT::GetServiceId","dvbsiparser/IISDB_SDTT::GetServiceId","mstv.iisdb_sdtt_getserviceid"]
old-location: mstv\iisdb_sdtt_getserviceid.htm
tech.root: mstv
ms.assetid: 36e9d2b7-f89a-47ad-9fd2-d9aa8d76949c
ms.date: 12/05/2018
ms.keywords: GetServiceId, GetServiceId method [Microsoft TV Technologies], GetServiceId method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetServiceId method, IISDB_SDTT.GetServiceId, IISDB_SDTT::GetServiceId, dvbsiparser/IISDB_SDTT::GetServiceId, mstv.iisdb_sdtt_getserviceid
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
 - IISDB_SDTT::GetServiceId
 - dvbsiparser/IISDB_SDTT::GetServiceId
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
 - IISDB_SDTT.GetServiceId
---

# IISDB_SDTT::GetServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Receives the service_id field that uniquely identifies a service from
  an Integrated Services Digital Broadcasting System
  (ISDB)  software download
  trigger table
  (SDTT).

## -parameters

### -param pwVal [out]

Receives the service_id value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>