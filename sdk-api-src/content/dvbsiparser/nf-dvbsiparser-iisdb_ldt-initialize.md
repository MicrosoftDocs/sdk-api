---
UID: NF:dvbsiparser.IISDB_LDT.Initialize
title: IISDB_LDT::Initialize
author: windows-sdk-content
description: Initializes the object using captured table section data for an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT).
old-location: mstv\iisdb_ldt_initialize.htm
old-project: mstv
ms.assetid: 6239688f-2300-4cdb-97cb-179f63efb933
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IISDB_LDT interface [Microsoft TV Technologies],Initialize method, IISDB_LDT.Initialize, IISDB_LDT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_LDT interface, dvbsiparser/IISDB_LDT::Initialize, mstv.iisdb_ldt_initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_LDT.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_LDT::Initialize


## -description



  Initializes the object using captured table section data
  for an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT).


## -parameters




### -param pSectionList [in]


  Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface
  of the <b>SectionList</b> object that contains the section data.



### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3">IISDB_LDT</a>



<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a>



<b>SectionList</b>
 

 

