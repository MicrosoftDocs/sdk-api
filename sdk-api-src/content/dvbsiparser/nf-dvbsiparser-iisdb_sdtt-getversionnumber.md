---
UID: NF:dvbsiparser.IISDB_SDTT.GetVersionNumber
title: IISDB_SDTT::GetVersionNumber (dvbsiparser.h)
description: Gets the version number for an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IISDB_SDTT interface","IISDB_SDTT interface [Microsoft TV Technologies]","GetVersionNumber method","IISDB_SDTT.GetVersionNumber","IISDB_SDTT::GetVersionNumber","dvbsiparser/IISDB_SDTT::GetVersionNumber","mstv.iisdb_sdtt_getversionnumber"]
old-location: mstv\iisdb_sdtt_getversionnumber.htm
tech.root: mstv
ms.assetid: 19b2234b-6836-42b7-9e64-a8212946c77b
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetVersionNumber method, IISDB_SDTT.GetVersionNumber, IISDB_SDTT::GetVersionNumber, dvbsiparser/IISDB_SDTT::GetVersionNumber, mstv.iisdb_sdtt_getversionnumber
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
 - IISDB_SDTT::GetVersionNumber
 - dvbsiparser/IISDB_SDTT::GetVersionNumber
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
 - IISDB_SDTT.GetVersionNumber
---

# IISDB_SDTT::GetVersionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the version number for an Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).

## -parameters

### -param pbVal [out]

Receives the version number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>