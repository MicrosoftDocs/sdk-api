---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IIsdbSiParser2::GetSDT


## -description


Gets a
  service description table (SDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDT
  lists the names and other parameters of the services in an MPEG-2 transport stream.


## -parameters




### -param tableId [in]

Table identifier for the type of table to retrieve. For an SDT, this value is 0x42 for an actual transport stream, or 0x46 for another stream.


### -param pwTransportStreamId

Pointer to the transport_stream_id field. This field value uniquely identifies the transport stream that contains the SDT.


### -param ppSDT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/a9824eb9-ec12-4a09-ba42-243fe19c0670">IISDB_SDT</a>
interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a9824eb9-ec12-4a09-ba42-243fe19c0670">IISDB_SDT</a>



<a href="https://msdn.microsoft.com/d8dfc713-aaa4-46b1-8eca-2e132a9d705f">IIsdbSiParser2</a>
 

 

