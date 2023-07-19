---
UID: NF:dvbsiparser.IISDB_BIT.GetCountOfTableDescriptors
title: IISDB_BIT::GetCountOfTableDescriptors (dvbsiparser.h)
description: Gets the broadcaster_descriptors_length field value from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","IISDB_BIT interface","IISDB_BIT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","IISDB_BIT.GetCountOfTableDescriptors","IISDB_BIT::GetCountOfTableDescriptors","dvbsiparser/IISDB_BIT::GetCountOfTableDescriptors","mstv.iisdb_bit_getcountoftabledescriptors"]
old-location: mstv\iisdb_bit_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 69b1851b-b8a9-4dfe-be6b-ffadd2a83b12
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IISDB_BIT interface, IISDB_BIT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IISDB_BIT.GetCountOfTableDescriptors, IISDB_BIT::GetCountOfTableDescriptors, dvbsiparser/IISDB_BIT::GetCountOfTableDescriptors, mstv.iisdb_bit_getcountoftabledescriptors
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
 - IISDB_BIT::GetCountOfTableDescriptors
 - dvbsiparser/IISDB_BIT::GetCountOfTableDescriptors
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
 - IISDB_BIT.GetCountOfTableDescriptors
---

# IISDB_BIT::GetCountOfTableDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the broadcaster_descriptors_length field value from
  an
  Integrated Services Digital Broadcasting (ISDB)
  broadcaster information table
  (BIT).

## -parameters

### -param pdwVal [out]

Receives the broadcaster_descriptors_length field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>