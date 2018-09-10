---
UID: NF:dvbsiparser.IIsdbSiParser2.GetLDT
title: IIsdbSiParser2::GetLDT
author: windows-sdk-content
description: Gets a linked description table (LDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An LDT contains data that is used to collect reference information from other tables.
old-location: mstv\iisdbsiparser2_getldt.htm
tech.root: mstv
ms.assetid: b4b91e95-cf0f-488b-9941-4d1d81dc7661
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetLDT, GetLDT method [Microsoft TV Technologies], GetLDT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetLDT method, IIsdbSiParser2.GetLDT, IIsdbSiParser2::GetLDT, dvbsiparser/IIsdbSiParser2::GetLDT, mstv.iisdbsiparser2_getldt
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
 - IIsdbSiParser2.GetLDT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbSiParser2::GetLDT


## -description


Gets a 
  linked description table (LDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An LDT contains data that is used to collect reference
  information from other tables.


## -parameters




### -param tableId [in]

Table identifier for the type of table to retrieve. For an LDT, this value is 0xC7.


### -param pwOriginalServiceId

Pointer to the original_service_id field for the LDT. This field contains an identifier for the service  for this transport stream.


### -param ppLDT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3">IISDB_LDT</a>interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3">IISDB_LDT</a>



<a href="https://msdn.microsoft.com/d8dfc713-aaa4-46b1-8eca-2e132a9d705f">IIsdbSiParser2</a>
 

 

