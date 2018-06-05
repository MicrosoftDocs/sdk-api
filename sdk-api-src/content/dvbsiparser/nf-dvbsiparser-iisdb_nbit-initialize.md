---
UID: NF:dvbsiparser.IISDB_NBIT.Initialize
title: IISDB_NBIT::Initialize
author: windows-sdk-content
description: Initializes the object by using captured table section data from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
old-location: mstv\iisdb_nbit_initialize.htm
old-project: mstv
ms.assetid: 8c4e3f53-1b32-4374-915f-15651259dd55
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IISDB_NBIT interface [Microsoft TV Technologies],Initialize method, IISDB_NBIT.Initialize, IISDB_NBIT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_NBIT interface, dvbsiparser/IISDB_NBIT::Initialize, mstv.iisdb_nbit_initialize
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_NBIT.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_NBIT::Initialize


## -description



  Initializes the object by using captured table section data
  from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
  


## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface 
of the <b>SectionList</b> object that contains the section data.


### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables
filter. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>



<a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a>



<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a>
 

 

