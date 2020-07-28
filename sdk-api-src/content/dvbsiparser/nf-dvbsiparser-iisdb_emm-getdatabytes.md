---
UID: NF:dvbsiparser.IISDB_EMM.GetDataBytes
title: IISDB_EMM::GetDataBytes (dvbsiparser.h)
description: Gets the data from an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
helpviewer_keywords: ["GetDataBytes","GetDataBytes method [Microsoft TV Technologies]","GetDataBytes method [Microsoft TV Technologies]","IISDB_EMM interface","IISDB_EMM interface [Microsoft TV Technologies]","GetDataBytes method","IISDB_EMM.GetDataBytes","IISDB_EMM::GetDataBytes","dvbsiparser/IISDB_EMM::GetDataBytes","mstv.iisdb_emm_getdatabytes"]
old-location: mstv\iisdb_emm_getdatabytes.htm
tech.root: mstv
ms.assetid: 71d92f83-f802-4b5c-a3de-4a2ad675318a
ms.date: 12/05/2018
ms.keywords: GetDataBytes, GetDataBytes method [Microsoft TV Technologies], GetDataBytes method [Microsoft TV Technologies],IISDB_EMM interface, IISDB_EMM interface [Microsoft TV Technologies],GetDataBytes method, IISDB_EMM.GetDataBytes, IISDB_EMM::GetDataBytes, dvbsiparser/IISDB_EMM::GetDataBytes, mstv.iisdb_emm_getdatabytes
f1_keywords:
- dvbsiparser/IISDB_EMM.GetDataBytes
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IISDB_EMM.GetDataBytes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_EMM::GetDataBytes


## -description


Gets the data 
  from an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table.
  


## -parameters




### -param pwBufferLength [in, out]

On input, specifies the length in bytes of the buffer (specified in the <i>pbBuffer</i> parameter) that receives the EMM table data. On output, gets the actual length of the data returned in <i>pbBuffer</i>.


### -param pbBuffer [out]

Receives the data from the EMM table.
The allocated size of this buffer must be greater than or equal to the value
that the <i>pwBufferLength</i> parameter points to.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a>
 

 

