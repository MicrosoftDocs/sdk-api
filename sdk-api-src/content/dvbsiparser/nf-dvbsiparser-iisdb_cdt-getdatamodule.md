---
UID: NF:dvbsiparser.IISDB_CDT.GetDataModule
title: IISDB_CDT::GetDataModule method
author: windows-driver-content
description: Receives the data module from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
old-location: mstv\iisdb_cdt_getdatamodule.htm
old-project: mstv
ms.assetid: b7ff7e8a-17bd-46aa-bf9b-74f3e33a7ce2
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetDataModule method [Microsoft TV Technologies], GetDataModule method [Microsoft TV Technologies], IISDB_CDT interface, GetDataModule,IISDB_CDT.GetDataModule, IISDB_CDT, IISDB_CDT interface [Microsoft TV Technologies], GetDataModule method, IISDB_CDT::GetDataModule, dvbsiparser/IISDB_CDT::GetDataModule, mstv.iisdb_cdt_getdatamodule
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
-	IISDB_CDT.GetDataModule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_CDT::GetDataModule method


## -description



  Receives the data module from
  an Integrated Services Digital Broadcasting (ISDB)
  common data table (CDT). 


## -parameters




### -param pbData [out]

Pointer to a memory block allocated to receive the data module.
The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>
 

 

