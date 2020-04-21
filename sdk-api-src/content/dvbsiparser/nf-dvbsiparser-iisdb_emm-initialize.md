---
UID: NF:dvbsiparser.IISDB_EMM.Initialize
title: IISDB_EMM::Initialize (dvbsiparser.h)
description: Initializes the data elements of an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table by using the list of MPEG-2 EMM sections.helpviewer_keywords: ["IISDB_EMM interface [Microsoft TV Technologies]","Initialize method","IISDB_EMM.Initialize","IISDB_EMM::Initialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IISDB_EMM interface","dvbsiparser/IISDB_EMM::Initialize","mstv.iisdb_emm_initialize"]
old-location: mstv\iisdb_emm_initialize.htm
tech.root: mstv
ms.assetid: 127e7987-6782-4577-9104-86124d948d18
ms.date: 12/05/2018
ms.keywords: IISDB_EMM interface [Microsoft TV Technologies],Initialize method, IISDB_EMM.Initialize, IISDB_EMM::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_EMM interface, dvbsiparser/IISDB_EMM::Initialize, mstv.iisdb_emm_initialize
f1_keywords:
- dvbsiparser/IISDB_EMM.Initialize
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
- IISDB_EMM.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_EMM::Initialize


## -description


Initializes the data elements of  an Integrated Services
  Digital Broadcasting (ISDB) entitlement management message (EMM) table
   by using the
  list of MPEG-2 EMM sections.



## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface for the
MPEG-2 ISDB EMM section list.


### -param pMPEGData [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables</a> filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_emm">IISDB_EMM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a>
 

 

