---
UID: NF:dvbsiparser.IIsdbSiParser2.GetCDT
title: IIsdbSiParser2::GetCDT method
author: windows-driver-content
description: Gets the common data table (CDT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A CDT contains data that is needed for receivers and stored in nonvolatile memory, such as company logos.
old-location: mstv\iisdbsiparser2_getcdt.htm
old-project: mstv
ms.assetid: c984a340-d31b-43a5-baac-323629002aab
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCDT method [Microsoft TV Technologies], GetCDT method [Microsoft TV Technologies], IIsdbSiParser2 interface, GetCDT,IIsdbSiParser2.GetCDT, IIsdbSiParser2, IIsdbSiParser2 interface [Microsoft TV Technologies], GetCDT method, IIsdbSiParser2::GetCDT, dvbsiparser/IIsdbSiParser2::GetCDT, mstv.iisdbsiparser2_getcdt
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
-	IIsdbSiParser2.GetCDT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSiParser2::GetCDT method


## -description


Gets the common data table (CDT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A CDT contains data that is needed for receivers and stored in
  nonvolatile memory, such as company logos.


## -parameters




### -param tableId [in]

Table identifier for the type of table to retrieve. For a CDT, this value is 0xC8.


### -param bSectionNumber [in]

Specifies the value of the section_number field for the CDT.


### -param pwDownloadDataId

Pointer to the download_data_id field value for the CDT.


### -param ppCDT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>
interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>



<a href="https://msdn.microsoft.com/d8dfc713-aaa4-46b1-8eca-2e132a9d705f">IIsdbSiParser2</a>
 

 

