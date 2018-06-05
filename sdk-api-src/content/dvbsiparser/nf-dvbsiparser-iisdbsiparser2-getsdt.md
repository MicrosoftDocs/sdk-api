---
UID: NF:dvbsiparser.IIsdbSiParser2.GetSDT
title: IIsdbSiParser2::GetSDT
author: windows-sdk-content
description: Gets a service description table (SDT) from an Integrated Services Digital Broadcast (ISDB) transport stream. An SDT lists the names and other parameters of the services in an MPEG-2 transport stream.
old-location: mstv\iisdbsiparser2_getsdt.htm
old-project: mstv
ms.assetid: d15d1b6a-5b53-4962-89a3-9bd06e00d366
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetSDT, GetSDT method [Microsoft TV Technologies], GetSDT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetSDT method, IIsdbSiParser2.GetSDT, IIsdbSiParser2::GetSDT, dvbsiparser/IIsdbSiParser2::GetSDT, mstv.iisdbsiparser2_getsdt
ms.prod: windows
ms.technology: windows-sdk
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
-	IIsdbSiParser2.GetSDT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

