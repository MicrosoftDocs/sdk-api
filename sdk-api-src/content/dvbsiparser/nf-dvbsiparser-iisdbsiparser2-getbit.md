---
UID: NF:dvbsiparser.IIsdbSiParser2.GetBIT
title: IIsdbSiParser2::GetBIT
author: windows-sdk-content
description: Gets the broadcaster information table (BIT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A BIT contains a broadcaster unit and the service information transmission parameter for each broadcaster unit.
old-location: mstv\iisdbsiparser2_getbit.htm
old-project: mstv
ms.assetid: 25993059-a1a9-486f-97b3-fd240c8931dc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetBIT, GetBIT method [Microsoft TV Technologies], GetBIT method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetBIT method, IIsdbSiParser2.GetBIT, IIsdbSiParser2::GetBIT, dvbsiparser/IIsdbSiParser2::GetBIT, mstv.iisdbsiparser2_getbit
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbSiParser2.GetBIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSiParser2::GetBIT


## -description


Gets the broadcaster information table (BIT) from an Integrated Services Digital Broadcasting (ISDB) transport stream. A BIT contains a broadcaster unit and the service information transmission parameter
  for each broadcaster unit.



## -parameters




### -param tableId [in]

Table identifier for the type of table to retrieve. For a BIT, this value is 0xC4.


### -param pwOriginalNetworkId

Pointer to the original_network_id field for the BIT. This field contains an identifier for the broadcaster that originates the
  MPEG-2 transport stream


### -param ppBIT [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0ec4497c-68c3-4b0e-a9e4-332e42b2c89b">IISDB_BIT</a>



<a href="https://msdn.microsoft.com/d8dfc713-aaa4-46b1-8eca-2e132a9d705f">IIsdbSiParser2</a>
 

 

