---
UID: NF:dvbsiparser.IPBDA_EIT.GetRecordDuration
title: IPBDA_EIT::GetRecordDuration (dvbsiparser.h)
description: Gets the duration from an event record in an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetRecordDuration","GetRecordDuration method [Microsoft TV Technologies]","GetRecordDuration method [Microsoft TV Technologies]","IPBDA_EIT interface","IPBDA_EIT interface [Microsoft TV Technologies]","GetRecordDuration method","IPBDA_EIT.GetRecordDuration","IPBDA_EIT::GetRecordDuration","dvbsiparser/IPBDA_EIT::GetRecordDuration","mstv.ipbda_eit_getrecordduration"]
old-location: mstv\ipbda_eit_getrecordduration.htm
tech.root: mstv
ms.assetid: 898e211c-3228-441d-a099-907676da4bbe
ms.date: 12/05/2018
ms.keywords: GetRecordDuration, GetRecordDuration method [Microsoft TV Technologies], GetRecordDuration method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetRecordDuration method, IPBDA_EIT.GetRecordDuration, IPBDA_EIT::GetRecordDuration, dvbsiparser/IPBDA_EIT::GetRecordDuration, mstv.ipbda_eit_getrecordduration
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
 - IPBDA_EIT::GetRecordDuration
 - dvbsiparser/IPBDA_EIT::GetRecordDuration
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
 - IPBDA_EIT.GetRecordDuration
---

# IPBDA_EIT::GetRecordDuration


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the duration from an event record in an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getcountofrecords">IPBDA_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.

### -param pmdVal [out]

Receives the event duration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>