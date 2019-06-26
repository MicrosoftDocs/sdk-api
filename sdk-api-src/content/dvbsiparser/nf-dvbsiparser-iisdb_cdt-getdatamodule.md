---
UID: NF:dvbsiparser.IISDB_CDT.GetDataModule
title: IISDB_CDT::GetDataModule (dvbsiparser.h)
author: windows-sdk-content
description: Receives the data module from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
old-location: mstv\iisdb_cdt_getdatamodule.htm
tech.root: mstv
ms.assetid: b7ff7e8a-17bd-46aa-bf9b-74f3e33a7ce2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDataModule, GetDataModule method [Microsoft TV Technologies], GetDataModule method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetDataModule method, IISDB_CDT.GetDataModule, IISDB_CDT::GetDataModule, dvbsiparser/IISDB_CDT::GetDataModule, mstv.iisdb_cdt_getdatamodule
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IISDB_CDT.GetDataModule"
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
 - IISDB_CDT.GetDataModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_CDT::GetDataModule


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>
 

 

