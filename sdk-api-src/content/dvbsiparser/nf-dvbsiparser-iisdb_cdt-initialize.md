---
UID: NF:dvbsiparser.IISDB_CDT.Initialize
title: IISDB_CDT::Initialize (dvbsiparser.h)
description: Initializes the object by using captured table section data from an Integrated Services Digital Broadcasting System (ISDB) common data table (CDT).
helpviewer_keywords: ["IISDB_CDT interface [Microsoft TV Technologies]","Initialize method","IISDB_CDT.Initialize","IISDB_CDT::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IISDB_CDT interface","dvbsiparser/IISDB_CDT::Initialize","mstv.iisdb_cdt_initialize"]
old-location: mstv\iisdb_cdt_initialize.htm
tech.root: mstv
ms.assetid: 0430d839-4b7f-4d1c-9e5b-bd794d67f065
ms.date: 12/05/2018
ms.keywords: IISDB_CDT interface [Microsoft TV Technologies],Initialize method, IISDB_CDT.Initialize, IISDB_CDT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_CDT interface, dvbsiparser/IISDB_CDT::Initialize, mstv.iisdb_cdt_initialize
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
 - IISDB_CDT::Initialize
 - dvbsiparser/IISDB_CDT::Initialize
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
 - IISDB_CDT.Initialize
---

# IISDB_CDT::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Initializes the object by using captured table section data
  from an Integrated Services Digital Broadcasting System
  (ISDB) common data table (CDT).

## -parameters

### -param pSectionList [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface
  of the object that contains the section data.

### -param pMPEGData [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the <a href="/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables</a> filter.

### -param bSectionNumber [in]

Specifies a value for the section_number field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>



<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a>



<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a>