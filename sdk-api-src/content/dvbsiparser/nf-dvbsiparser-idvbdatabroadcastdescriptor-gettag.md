---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetTag
title: IDvbDataBroadcastDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast descriptor.
old-location: mstv\idvbdatabroadcastdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 8f49a4c3-8e40-4cb2-ba3c-ef0b945243f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbDataBroadcastDescriptor.GetTag, IDvbDataBroadcastDescriptor::GetTag, dvbsiparser/IDvbDataBroadcastDescriptor::GetTag, mstv.idvbdatabroadcastdescriptor_gettag
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
 - IDvbDataBroadcastDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbDataBroadcastDescriptor::GetTag


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast descriptor. 


## -parameters




### -param pbVal [out]

Receives the descriptor tag. For data broadcast descriptors, this value is 0x64.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b1d2711-e5ad-4d4c-bc8f-e199bcd75799">IDvbDataBroadcastDescriptor</a>
 

 

