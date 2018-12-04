---
UID: NF:dvbsiparser.IIsdbSiParser2.GetEMM
title: IIsdbSiParser2::GetEMM
author: windows-sdk-content
description: Gets the entitlement management message (EMM) table from an Integrated Services Digital Broadcast (ISDB) transport stream.
old-location: mstv\iisdbsiparser2_getemm.htm
tech.root: mstv
ms.assetid: 9dc2aaa9-50f0-4c72-a252-3757a1aa13b7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetEMM, GetEMM method [Microsoft TV Technologies], GetEMM method [Microsoft TV Technologies],IIsdbSiParser2 interface, IIsdbSiParser2 interface [Microsoft TV Technologies],GetEMM method, IIsdbSiParser2.GetEMM, IIsdbSiParser2::GetEMM, dvbsiparser/IIsdbSiParser2::GetEMM, mstv.iisdbsiparser2_getemm
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
 - IIsdbSiParser2.GetEMM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbSiParser2::GetEMM


## -description


 
  Gets the entitlement management message (EMM) table from an Integrated Services Digital Broadcast (ISDB) transport stream. An EMM contains conditional access data, such as contract
  information for subscribers, keys to decrypt common information, and the
  authorization levels or services of specific decoders.



## -parameters




### -param pid [in]

Specifies the packet identifier (PID) of the transport stream packet that transmits the EMM.


### -param wTableIdExt [in]

Value of the table_id field for the EMM. This field value identifies a subtable in the EMM.


### -param ppEMM [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/a1389e7c-a3f1-4782-b811-5e09615b3e47">IISDB_EMM</a>interface. Use this interface to retrieve the information in the table. 
The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1389e7c-a3f1-4782-b811-5e09615b3e47">IISDB_EMM</a>



<a href="https://msdn.microsoft.com/d8dfc713-aaa4-46b1-8eca-2e132a9d705f">IIsdbSiParser2</a>
 

 

