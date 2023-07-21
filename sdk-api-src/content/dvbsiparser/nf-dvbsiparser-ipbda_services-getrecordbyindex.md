---
UID: NF:dvbsiparser.IPBDA_Services.GetRecordByIndex
title: IPBDA_Services::GetRecordByIndex (dvbsiparser.h)
description: Gets a service record at a given position from a Program and System Information Protocol (PSIP) table in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetRecordByIndex","GetRecordByIndex method [Microsoft TV Technologies]","GetRecordByIndex method [Microsoft TV Technologies]","IPBDA_Services interface","IPBDA_Services interface [Microsoft TV Technologies]","GetRecordByIndex method","IPBDA_Services.GetRecordByIndex","IPBDA_Services::GetRecordByIndex","dvbsiparser/IPBDA_Services::GetRecordByIndex","mstv.ipbda_services_getrecordbyindex"]
old-location: mstv\ipbda_services_getrecordbyindex.htm
tech.root: mstv
ms.assetid: 1f9a71a4-3cfd-4a08-929f-e17d506a021b
ms.date: 12/05/2018
ms.keywords: GetRecordByIndex, GetRecordByIndex method [Microsoft TV Technologies], GetRecordByIndex method [Microsoft TV Technologies],IPBDA_Services interface, IPBDA_Services interface [Microsoft TV Technologies],GetRecordByIndex method, IPBDA_Services.GetRecordByIndex, IPBDA_Services::GetRecordByIndex, dvbsiparser/IPBDA_Services::GetRecordByIndex, mstv.ipbda_services_getrecordbyindex
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
 - IPBDA_Services::GetRecordByIndex
 - dvbsiparser/IPBDA_Services::GetRecordByIndex
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
 - IPBDA_Services.GetRecordByIndex
---

# IPBDA_Services::GetRecordByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a service record at a given position from a  Program and System Information Protocol (PSIP) table in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_services-getcountofrecords">IPBDA_Services::GetCountOfRecords</a> method to get the number of records in the PSIP table.

### -param pul64ServiceIdx [out]

Receives the service record at the position given by <i>dwRecordIndex</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_services">IPBDA_Services</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_services-getcountofrecords">IPBDA_Services::GetCountOfRecords</a>