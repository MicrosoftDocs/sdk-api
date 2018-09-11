---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetSelectorBytes
title: IDvbDataBroadcastDescriptor::GetSelectorBytes
author: windows-sdk-content
description: Gets the data from the selector in a Digital Video Broadcast (DVB) data broadcast descriptor. The selector is defined by the broadcast standard for the network.
old-location: mstv\idvbdatabroadcastdescriptor_getselectorbytes.htm
tech.root: mstv
ms.assetid: 72fca5a8-2ea5-4000-8b00-dbd408cba602
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSelectorBytes, GetSelectorBytes method [Microsoft TV Technologies], GetSelectorBytes method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetSelectorBytes method, IDvbDataBroadcastDescriptor.GetSelectorBytes, IDvbDataBroadcastDescriptor::GetSelectorBytes, dvbsiparser/IDvbDataBroadcastDescriptor::GetSelectorBytes, mstv.idvbdatabroadcastdescriptor_getselectorbytes
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
 - IDvbDataBroadcastDescriptor.GetSelectorBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbDataBroadcastDescriptor::GetSelectorBytes


## -description


Gets the data from the selector in a Digital Video Broadcast (DVB) data broadcast descriptor. The selector is defined by the broadcast standard for the network.


## -parameters




### -param pbLen [in, out]

On input, specifies the size of the buffer (pointed to by the <i>pbVal</i> parameter) allocated for the selector data, in bytes. On output, gets the actual length of the selector data.


### -param pbVal [out]

Receives the selector bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b1d2711-e5ad-4d4c-bc8f-e199bcd75799">IDvbDataBroadcastDescriptor</a>
 

 

