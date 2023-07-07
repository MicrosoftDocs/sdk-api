---
UID: NF:dvbsiparser.IISDB_EMM.GetVersionNumber
title: IISDB_EMM::GetVersionNumber (dvbsiparser.h)
description: Gets the version number for an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IISDB_EMM interface","IISDB_EMM interface [Microsoft TV Technologies]","GetVersionNumber method","IISDB_EMM.GetVersionNumber","IISDB_EMM::GetVersionNumber","dvbsiparser/IISDB_EMM::GetVersionNumber","mstv.iisdb_emm_getversionnumber"]
old-location: mstv\iisdb_emm_getversionnumber.htm
tech.root: mstv
ms.assetid: 3eebc1cc-044b-4a0a-8259-cb225f829df8
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IISDB_EMM interface, IISDB_EMM interface [Microsoft TV Technologies],GetVersionNumber method, IISDB_EMM.GetVersionNumber, IISDB_EMM::GetVersionNumber, dvbsiparser/IISDB_EMM::GetVersionNumber, mstv.iisdb_emm_getversionnumber
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
 - IISDB_EMM::GetVersionNumber
 - dvbsiparser/IISDB_EMM::GetVersionNumber
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
 - IISDB_EMM.GetVersionNumber
---

# IISDB_EMM::GetVersionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the version number for an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table.

## -parameters

### -param pbVal [out]

Receives the version_number field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a>