---
UID: NF:dvbsiparser.IIsdbSiParser2.GetSDTT
title: IIsdbSiParser2::GetSDTT
author: windows-driver-content
description: Gets the software download trigger table (SDTT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDTT contains download information such as the service identifier, schedule, and receiver types for revision.
old-location: mstv\iisdbsiparser2_getsdtt.htm
old-project: mstv
ms.assetid: fd361526-eb0c-4edd-b346-3bded48fdc06
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetSDTT, GetSDTT method [Microsoft TV Technologies], GetSDTT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetSDTT method, IIsdbSiParser2.GetSDTT, IIsdbSiParser2::GetSDTT, dvbsiparser/IIsdbSiParser2::GetSDTT, mstv.iisdbsiparser2_getsdtt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	IIsdbSiParser2.GetSDTT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSiParser2::GetSDTT


## -description


  Gets the software download
  trigger table
  (SDTT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDTT contains download information such as the service identifier, schedule, and
  receiver types for revision.



## -parameters




### -param tableId [in]

Table identifier for the type of table to retrieve. For an SDTT, this value is 0xC34.


### -param pwTableIdExt

Value of the table_id_extension field for the SDTT. This field value identifies a specific instance of the SDTT.


### -param ppSDTT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>
interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>



<a href="https://msdn.microsoft.com/d8dfc713-aaa4-46b1-8eca-2e132a9d705f">IIsdbSiParser2</a>
 

 

