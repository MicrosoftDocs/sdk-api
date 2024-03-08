---
UID: NF:dvbsiparser.IISDB_EMM.GetSharedEmmMessage
title: IISDB_EMM::GetSharedEmmMessage (dvbsiparser.h)
description: Gets a shared message from an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
helpviewer_keywords: ["GetSharedEmmMessage","GetSharedEmmMessage method [Microsoft TV Technologies]","GetSharedEmmMessage method [Microsoft TV Technologies]","IISDB_EMM interface","IISDB_EMM interface [Microsoft TV Technologies]","GetSharedEmmMessage method","IISDB_EMM.GetSharedEmmMessage","IISDB_EMM::GetSharedEmmMessage","dvbsiparser/IISDB_EMM::GetSharedEmmMessage","mstv.iisdb_emm_getsharedemmmessage"]
old-location: mstv\iisdb_emm_getsharedemmmessage.htm
tech.root: mstv
ms.assetid: d3ad405c-cdf0-4a37-9495-3f126e6c0688
ms.date: 12/05/2018
ms.keywords: GetSharedEmmMessage, GetSharedEmmMessage method [Microsoft TV Technologies], GetSharedEmmMessage method [Microsoft TV Technologies],IISDB_EMM interface, IISDB_EMM interface [Microsoft TV Technologies],GetSharedEmmMessage method, IISDB_EMM.GetSharedEmmMessage, IISDB_EMM::GetSharedEmmMessage, dvbsiparser/IISDB_EMM::GetSharedEmmMessage, mstv.iisdb_emm_getsharedemmmessage
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
 - IISDB_EMM::GetSharedEmmMessage
 - dvbsiparser/IISDB_EMM::GetSharedEmmMessage
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
 - IISDB_EMM.GetSharedEmmMessage
---

# IISDB_EMM::GetSharedEmmMessage


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a shared message from an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table.

## -parameters

### -param pwLength [out]

Receives the length of the buffer required to hold the message.

### -param ppbMessage [out]

Pointer to a memory block allocated to receive the shared message object.
  The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a>