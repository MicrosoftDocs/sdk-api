---
UID: NF:dvbsiparser.IISDB_NBIT.Initialize
title: IISDB_NBIT::Initialize (dvbsiparser.h)
description: Initializes the object by using captured table section data from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
helpviewer_keywords: ["IISDB_NBIT interface [Microsoft TV Technologies]","Initialize method","IISDB_NBIT.Initialize","IISDB_NBIT::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IISDB_NBIT interface","dvbsiparser/IISDB_NBIT::Initialize","mstv.iisdb_nbit_initialize"]
old-location: mstv\iisdb_nbit_initialize.htm
tech.root: mstv
ms.assetid: 8c4e3f53-1b32-4374-915f-15651259dd55
ms.date: 12/05/2018
ms.keywords: IISDB_NBIT interface [Microsoft TV Technologies],Initialize method, IISDB_NBIT.Initialize, IISDB_NBIT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_NBIT interface, dvbsiparser/IISDB_NBIT::Initialize, mstv.iisdb_nbit_initialize
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
 - IISDB_NBIT::Initialize
 - dvbsiparser/IISDB_NBIT::Initialize
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
 - IISDB_NBIT.Initialize
---

# IISDB_NBIT::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Initializes the object by using captured table section data
  from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).

## -parameters

### -param pSectionList [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface 
of the <b>SectionList</b> object that contains the section data.

### -param pMPEGData [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables
filter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_nbit">IISDB_NBIT</a>



<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a>



<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a>