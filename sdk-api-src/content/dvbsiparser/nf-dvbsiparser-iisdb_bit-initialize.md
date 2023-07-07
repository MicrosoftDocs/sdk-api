---
UID: NF:dvbsiparser.IISDB_BIT.Initialize
title: IISDB_BIT::Initialize (dvbsiparser.h)
description: Initializes the object by using captured table section data for an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
helpviewer_keywords: ["IISDB_BIT interface [Microsoft TV Technologies]","Initialize method","IISDB_BIT.Initialize","IISDB_BIT::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IISDB_BIT interface","dvbsiparser/IISDB_BIT::Initialize","mstv.iisdb_bit_initialize"]
old-location: mstv\iisdb_bit_initialize.htm
tech.root: mstv
ms.assetid: 1c38cbc0-4e47-4f15-9a9b-548e74af6462
ms.date: 12/05/2018
ms.keywords: IISDB_BIT interface [Microsoft TV Technologies],Initialize method, IISDB_BIT.Initialize, IISDB_BIT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_BIT interface, dvbsiparser/IISDB_BIT::Initialize, mstv.iisdb_bit_initialize
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
 - IISDB_BIT::Initialize
 - dvbsiparser/IISDB_BIT::Initialize
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
 - IISDB_BIT.Initialize
---

# IISDB_BIT::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Initializes the object by using captured table section data
  for an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT).

## -parameters

### -param pSectionList [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface
  of the <b>SectionList</b> object that contains the section data.

### -param pMPEGData [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_bit">IISDB_BIT</a>