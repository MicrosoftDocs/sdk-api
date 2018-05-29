---
UID: NF:dvbsiparser.IISDB_SDTT.Initialize
title: IISDB_SDTT::Initialize
author: windows-sdk-content
description: Initializes the object by using captured table section data from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_initialize.htm
old-project: mstv
ms.assetid: f1018e3a-00dd-4964-b491-0193a71e7d51
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IISDB_SDTT interface [Microsoft TV Technologies],Initialize method, IISDB_SDTT.Initialize, IISDB_SDTT::Initialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IISDB_SDTT interface, dvbsiparser/IISDB_SDTT::Initialize, mstv.iisdb_sdtt_initialize
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_SDTT.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDTT::Initialize


## -description



  Initializes the object by using captured table section data from
  an Integrated Services Digital Broadcasting (ISDB) software download
  trigger table
  (SDTT). 


## -parameters




### -param pSectionList [in]


  Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface
  of the object that contains the section data.



### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the <a href="https://msdn.microsoft.com/03027748-03da-485c-8787-3cf171fff1e0">MPEG-2 Sections and Tables</a> filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a>
 

 

