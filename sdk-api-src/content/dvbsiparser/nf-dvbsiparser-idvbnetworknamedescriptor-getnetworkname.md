---
UID: NF:dvbsiparser.IDvbNetworkNameDescriptor.GetNetworkName
title: IDvbNetworkNameDescriptor::GetNetworkName
author: windows-sdk-content
description: Gets the network name, in ASCII string format, from a Digital Video Broadcast (DVB) network name descriptor.
old-location: mstv\idvbnetworknamedescriptor_getnetworkname.htm
old-project: mstv
ms.assetid: 261a6c65-65a5-43ed-aaed-12968b996c5a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetNetworkName, GetNetworkName method [Microsoft TV Technologies], GetNetworkName method [Microsoft TV Technologies],IDvbNetworkNameDescriptor interface, IDvbNetworkNameDescriptor interface [Microsoft TV Technologies],GetNetworkName method, IDvbNetworkNameDescriptor.GetNetworkName, IDvbNetworkNameDescriptor::GetNetworkName, dvbsiparser/IDvbNetworkNameDescriptor::GetNetworkName, mstv.idvbnetworknamedescriptor_getnetworkname
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbNetworkNameDescriptor.GetNetworkName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbNetworkNameDescriptor::GetNetworkName


## -description


Gets the network name, in ASCII string format, from a Digital Video Broadcast (DVB) network name  descriptor.


## -parameters




### -param pszName

Pointer to a buffer that receives the network name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b80892d-05e6-4776-932a-a9e2bf985984">IDvbNetworkNameDescriptor</a>
 

 

