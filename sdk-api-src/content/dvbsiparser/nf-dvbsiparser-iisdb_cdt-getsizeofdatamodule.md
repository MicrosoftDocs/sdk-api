---
UID: NF:dvbsiparser.IISDB_CDT.GetSizeOfDataModule
title: IISDB_CDT::GetSizeOfDataModule (dvbsiparser.h)
description: Gets the size of a data module from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
helpviewer_keywords: ["GetSizeOfDataModule","GetSizeOfDataModule method [Microsoft TV Technologies]","GetSizeOfDataModule method [Microsoft TV Technologies]","IISDB_CDT interface","IISDB_CDT interface [Microsoft TV Technologies]","GetSizeOfDataModule method","IISDB_CDT.GetSizeOfDataModule","IISDB_CDT::GetSizeOfDataModule","dvbsiparser/IISDB_CDT::GetSizeOfDataModule","mstv.iisdb_cdt_getsizeofdatamodule"]
old-location: mstv\iisdb_cdt_getsizeofdatamodule.htm
tech.root: mstv
ms.assetid: c05a8c14-f0da-49d7-be34-1cac435a98da
ms.date: 12/05/2018
ms.keywords: GetSizeOfDataModule, GetSizeOfDataModule method [Microsoft TV Technologies], GetSizeOfDataModule method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetSizeOfDataModule method, IISDB_CDT.GetSizeOfDataModule, IISDB_CDT::GetSizeOfDataModule, dvbsiparser/IISDB_CDT::GetSizeOfDataModule, mstv.iisdb_cdt_getsizeofdatamodule
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
 - IISDB_CDT::GetSizeOfDataModule
 - dvbsiparser/IISDB_CDT::GetSizeOfDataModule
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
 - IISDB_CDT.GetSizeOfDataModule
---

# IISDB_CDT::GetSizeOfDataModule


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the size of a data module 
  from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).

## -parameters

### -param pdwVal [out]

Receives the size of the data module.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>