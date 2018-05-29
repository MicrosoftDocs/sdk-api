---
UID: NF:dvbsiparser.IDvbNetworkNameDescriptor.GetTag
title: IDvbNetworkNameDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) network name descriptor.
old-location: mstv\idvbnetworknamedescriptor_gettag.htm
old-project: mstv
ms.assetid: 9bc0ffea-ef18-488e-adeb-a5fd19b343a6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbNetworkNameDescriptor interface, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbNetworkNameDescriptor.GetTag, IDvbNetworkNameDescriptor::GetTag, dvbsiparser/IDvbNetworkNameDescriptor::GetTag, mstv.idvbnetworknamedescriptor_gettag
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbNetworkNameDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbNetworkNameDescriptor::GetTag


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) network name descriptor.


## -parameters




### -param pbVal [out]

Receives the identifier tag. For DVB network name descriptors, this value is "0x40".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b80892d-05e6-4776-932a-a9e2bf985984">IDvbNetworkNameDescriptor</a>
 

 

