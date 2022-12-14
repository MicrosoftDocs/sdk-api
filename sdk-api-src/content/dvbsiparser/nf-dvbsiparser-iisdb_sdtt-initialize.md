---
UID: NF:dvbsiparser.IISDB_SDTT.Initialize
title: IISDB_SDTT::Initialize (dvbsiparser.h)
description: Initializes the object by using captured table section data from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
helpviewer_keywords: ["IISDB_SDTT interface [Microsoft TV Technologies]","Initialize method","IISDB_SDTT.Initialize","IISDB_SDTT::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IISDB_SDTT interface","dvbsiparser/IISDB_SDTT::Initialize","mstv.iisdb_sdtt_initialize"]
old-location: mstv\iisdb_sdtt_initialize.htm
tech.root: mstv
ms.assetid: f1018e3a-00dd-4964-b491-0193a71e7d51
ms.date: 12/05/2018
ms.keywords: IISDB_SDTT interface [Microsoft TV Technologies],Initialize method, IISDB_SDTT.Initialize, IISDB_SDTT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_SDTT interface, dvbsiparser/IISDB_SDTT::Initialize, mstv.iisdb_sdtt_initialize
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
 - IISDB_SDTT::Initialize
 - dvbsiparser/IISDB_SDTT::Initialize
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
 - IISDB_SDTT.Initialize
---

# IISDB_SDTT::Initialize


## -description

Initializes the object by using captured table section data from
  an Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT).

## -parameters

### -param pSectionList [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface
  of the object that contains the section data.

### -param pMPEGData [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the <a href="/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables</a> filter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_sdtt">IISDB_SDTT</a>



<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a>