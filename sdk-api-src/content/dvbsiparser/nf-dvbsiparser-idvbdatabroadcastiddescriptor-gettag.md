---
UID: NF:dvbsiparser.IDvbDataBroadcastIDDescriptor.GetTag
title: IDvbDataBroadcastIDDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast ID descriptor.
old-location: mstv\idvbdatabroadcastiddescriptor_gettag.htm
tech.root: MSTV
ms.assetid: 7c3c13f0-03b0-47fe-bd87-5bb6d32ef838
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbDataBroadcastIDDescriptor interface, IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbDataBroadcastIDDescriptor.GetTag, IDvbDataBroadcastIDDescriptor::GetTag, dvbsiparser/IDvbDataBroadcastIDDescriptor::GetTag, mstv.idvbdatabroadcastiddescriptor_gettag
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDvbDataBroadcastIDDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbDataBroadcastIDDescriptor::GetTag


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast ID descriptor. 


## -parameters




### -param pbVal [out]

Receives the descriptor tag. For data broadcast ID descriptors, this value is 0x66.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8d46cffc-cb49-4749-a1b7-e05d5d90941f">IDvbDataBroadcastIDDescriptor</a>
 

 

