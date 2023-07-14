---
UID: NF:dvbsiparser.IISDB_LDT.GetOriginalServiceId
title: IISDB_LDT::GetOriginalServiceId (dvbsiparser.h)
description: Gets the original_service_id field from an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
helpviewer_keywords: ["GetOriginalServiceId","GetOriginalServiceId method [Microsoft TV Technologies]","GetOriginalServiceId method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetOriginalServiceId method","IISDB_LDT.GetOriginalServiceId","IISDB_LDT::GetOriginalServiceId","dvbsiparser/IISDB_LDT::GetOriginalServiceId","mstv.iisdb_ldt_getoriginalserviceid"]
old-location: mstv\iisdb_ldt_getoriginalserviceid.htm
tech.root: mstv
ms.assetid: 030c01e3-6149-4a61-aeb2-01143642213b
ms.date: 12/05/2018
ms.keywords: GetOriginalServiceId, GetOriginalServiceId method [Microsoft TV Technologies], GetOriginalServiceId method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetOriginalServiceId method, IISDB_LDT.GetOriginalServiceId, IISDB_LDT::GetOriginalServiceId, dvbsiparser/IISDB_LDT::GetOriginalServiceId, mstv.iisdb_ldt_getoriginalserviceid
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
 - IISDB_LDT::GetOriginalServiceId
 - dvbsiparser/IISDB_LDT::GetOriginalServiceId
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
 - IISDB_LDT.GetOriginalServiceId
---

# IISDB_LDT::GetOriginalServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the original_service_id field from
  an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT).

## -parameters

### -param pwVal [out]

Receives the original_service_id value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>