---
UID: NF:dvbsiparser.IPBDA_Services.GetCountOfRecords
title: IPBDA_Services::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of service records from a Program and System Information Protocol (PSIP) table in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IPBDA_Services interface","IPBDA_Services interface [Microsoft TV Technologies]","GetCountOfRecords method","IPBDA_Services.GetCountOfRecords","IPBDA_Services::GetCountOfRecords","dvbsiparser/IPBDA_Services::GetCountOfRecords","mstv.ipbda_services_getcountofrecords"]
old-location: mstv\ipbda_services_getcountofrecords.htm
tech.root: mstv
ms.assetid: a39a0ec2-aabc-4609-91cc-667c14773515
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IPBDA_Services interface, IPBDA_Services interface [Microsoft TV Technologies],GetCountOfRecords method, IPBDA_Services.GetCountOfRecords, IPBDA_Services::GetCountOfRecords, dvbsiparser/IPBDA_Services::GetCountOfRecords, mstv.ipbda_services_getcountofrecords
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
 - IPBDA_Services::GetCountOfRecords
 - dvbsiparser/IPBDA_Services::GetCountOfRecords
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
 - IPBDA_Services.GetCountOfRecords
---

# IPBDA_Services::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of service records from a  Program and System Information Protocol (PSIP) table in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param pdwVal [out]

Receives the number of service records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_services">IPBDA_Services</a>