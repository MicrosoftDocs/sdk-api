---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetONId
title: IDvbLinkageDescriptor::GetONId
author: windows-driver-content
description: Gets the network identifier of the broadcast system that originated an information service from a Digital Video Broadcast (DVB) linkage descriptor.
old-location: mstv\idvblinkagedescriptor_getonid.htm
old-project: mstv
ms.assetid: e7c27f45-032a-46d5-b5ae-8a4ef2ee2ebc
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetONId, GetONId method [Microsoft TV Technologies], GetONId method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetONId method, IDvbLinkageDescriptor.GetONId, IDvbLinkageDescriptor::GetONId, dvbsiparser/IDvbLinkageDescriptor::GetONId, mstv.idvblinkagedescriptor_getonid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
-	IDvbLinkageDescriptor.GetONId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLinkageDescriptor::GetONId


## -description


Gets the network identifier of the  broadcast system that originated an information service from a Digital Video Broadcast (DVB) linkage descriptor.


## -parameters




### -param pwVal [out]

Receives the network identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4e419b50-b9c2-48e4-a484-f0fcf5c9cb7f">IDvbLinkageDescriptor</a>
 

 

