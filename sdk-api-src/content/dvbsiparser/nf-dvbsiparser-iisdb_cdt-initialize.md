---
UID: NF:dvbsiparser.IISDB_CDT.Initialize
title: IISDB_CDT::Initialize
author: windows-sdk-content
description: Initializes the object by using captured table section data from an Integrated Services Digital Broadcasting System (ISDB) common data table (CDT).
old-location: mstv\iisdb_cdt_initialize.htm
tech.root: mstv
ms.assetid: 0430d839-4b7f-4d1c-9e5b-bd794d67f065
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IISDB_CDT interface [Microsoft TV Technologies],Initialize method, IISDB_CDT.Initialize, IISDB_CDT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_CDT interface, dvbsiparser/IISDB_CDT::Initialize, mstv.iisdb_cdt_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IISDB_CDT.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_CDT::Initialize


## -description


Initializes the object by using captured table section data
  from an Integrated Services Digital Broadcasting System
  (ISDB) common data table (CDT). 


## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface
  of the object that contains the section data.



### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the <a href="https://msdn.microsoft.com/03027748-03da-485c-8787-3cf171fff1e0">MPEG-2 Sections and Tables</a> filter.


### -param bSectionNumber [in]

Specifies a value for the section_number field.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>



<a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a>



<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a>
 

 

