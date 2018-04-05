---
UID: NF:dvbsiparser.IISDB_BIT.Initialize
title: IISDB_BIT::Initialize method
author: windows-driver-content
description: Initializes the object by using captured table section data for an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT).
old-location: mstv\iisdb_bit_initialize.htm
old-project: mstv
ms.assetid: 1c38cbc0-4e47-4f15-9a9b-548e74af6462
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IISDB_BIT, IISDB_BIT interface [Microsoft TV Technologies], Initialize method, IISDB_BIT::Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies], IISDB_BIT interface, Initialize,IISDB_BIT.Initialize, dvbsiparser/IISDB_BIT::Initialize, mstv.iisdb_bit_initialize
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_BIT.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_BIT::Initialize method


## -description



  Initializes the object by using captured table section data
  for an Integrated Services Digital Broadcasting (ISDB) broadcaster
  information table
  (BIT). 



## -parameters




### -param pSectionList [in]


  Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface
  of the <b>SectionList</b> object that contains the section data.



### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>
 

 

