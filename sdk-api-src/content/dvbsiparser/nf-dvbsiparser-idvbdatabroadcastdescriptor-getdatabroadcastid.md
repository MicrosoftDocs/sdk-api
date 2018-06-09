---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetDataBroadcastID
title: IDvbDataBroadcastDescriptor::GetDataBroadcastID
author: windows-sdk-content
description: Gets the identifier that identifies the network broadcast from a Digital Video Broadcast (DVB) data broadcast descriptor.
old-location: mstv\idvbdatabroadcastdescriptor_getdatabroadcastid.htm
old-project: mstv
ms.assetid: 0124e197-85a0-47bf-afb6-100c344e9c9e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetDataBroadcastID, GetDataBroadcastID method [Microsoft TV Technologies], GetDataBroadcastID method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetDataBroadcastID method, IDvbDataBroadcastDescriptor.GetDataBroadcastID, IDvbDataBroadcastDescriptor::GetDataBroadcastID, dvbsiparser/IDvbDataBroadcastDescriptor::GetDataBroadcastID, mstv.idvbdatabroadcastdescriptor_getdatabroadcastid
ms.prod: windows
ms.technology: windows-sdk
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
 - IDvbDataBroadcastDescriptor.GetDataBroadcastID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbDataBroadcastDescriptor::GetDataBroadcastID


## -description


Gets the identifier that identifies the network broadcast from a Digital Video
Broadcast (DVB) data broadcast descriptor.  


## -parameters




### -param pwVal [out]

Receives the broadcaster ID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b1d2711-e5ad-4d4c-bc8f-e199bcd75799">IDvbDataBroadcastDescriptor</a>
 

 

