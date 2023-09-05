---
UID: NF:dvbsiparser.IPBDA_EIT.GetRecordStartTime
title: IPBDA_EIT::GetRecordStartTime (dvbsiparser.h)
description: Gets the start time from an event record in an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetRecordStartTime","GetRecordStartTime method [Microsoft TV Technologies]","GetRecordStartTime method [Microsoft TV Technologies]","IPBDA_EIT interface","IPBDA_EIT interface [Microsoft TV Technologies]","GetRecordStartTime method","IPBDA_EIT.GetRecordStartTime","IPBDA_EIT::GetRecordStartTime","dvbsiparser/IPBDA_EIT::GetRecordStartTime","mstv.ipbda_eit_getrecordstarttime"]
old-location: mstv\ipbda_eit_getrecordstarttime.htm
tech.root: mstv
ms.assetid: 7022ac7c-b0ea-4ca1-931f-b09906f67df7
ms.date: 12/05/2018
ms.keywords: GetRecordStartTime, GetRecordStartTime method [Microsoft TV Technologies], GetRecordStartTime method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetRecordStartTime method, IPBDA_EIT.GetRecordStartTime, IPBDA_EIT::GetRecordStartTime, dvbsiparser/IPBDA_EIT::GetRecordStartTime, mstv.ipbda_eit_getrecordstarttime
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
 - IPBDA_EIT::GetRecordStartTime
 - dvbsiparser/IPBDA_EIT::GetRecordStartTime
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
 - IPBDA_EIT.GetRecordStartTime
---

# IPBDA_EIT::GetRecordStartTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the start time from an event record in an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getcountofrecords">IPBDA_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.

### -param pmdtVal [out]

Pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_date_and_time">MPEG_DATE_AND_TIME</a> structure that receives the start time from the event record.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>