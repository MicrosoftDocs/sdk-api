---
UID: NF:dvbsiparser.IISDB_LDT.GetVersionNumber
title: IISDB_LDT::GetVersionNumber (dvbsiparser.h)
description: Gets the version number for an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IISDB_LDT interface","IISDB_LDT interface [Microsoft TV Technologies]","GetVersionNumber method","IISDB_LDT.GetVersionNumber","IISDB_LDT::GetVersionNumber","dvbsiparser/IISDB_LDT::GetVersionNumber","mstv.iisdb_ldt_getversionnumber"]
old-location: mstv\iisdb_ldt_getversionnumber.htm
tech.root: mstv
ms.assetid: 7567ca34-2898-4066-a81c-348e3ac5c066
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IISDB_LDT interface, IISDB_LDT interface [Microsoft TV Technologies],GetVersionNumber method, IISDB_LDT.GetVersionNumber, IISDB_LDT::GetVersionNumber, dvbsiparser/IISDB_LDT::GetVersionNumber, mstv.iisdb_ldt_getversionnumber
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
 - IISDB_LDT::GetVersionNumber
 - dvbsiparser/IISDB_LDT::GetVersionNumber
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
 - IISDB_LDT.GetVersionNumber
---

# IISDB_LDT::GetVersionNumber


## -description

Gets the version number for an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT).

## -parameters

### -param pbVal [out]

Receives the version_number field.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>