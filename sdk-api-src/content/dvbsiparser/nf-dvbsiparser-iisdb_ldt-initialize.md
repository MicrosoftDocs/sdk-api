---
UID: NF:dvbsiparser.IISDB_LDT.Initialize
title: IISDB_LDT::Initialize (dvbsiparser.h)
author: windows-sdk-content
description: Initializes the object using captured table section data for an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
old-location: mstv\iisdb_ldt_initialize.htm
tech.root: mstv
ms.assetid: 6239688f-2300-4cdb-97cb-179f63efb933
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IISDB_LDT interface [Microsoft TV Technologies],Initialize method, IISDB_LDT.Initialize, IISDB_LDT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_LDT interface, dvbsiparser/IISDB_LDT::Initialize, mstv.iisdb_ldt_initialize
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IISDB_LDT.Initialize"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_LDT.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_LDT::Initialize


## -description


Initializes the object using captured table section data
  for an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT).


## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface
  of the <b>SectionList</b> object that contains the section data.



### -param pMPEGData [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_ldt">IISDB_LDT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a>



<b>SectionList</b>
 

 

