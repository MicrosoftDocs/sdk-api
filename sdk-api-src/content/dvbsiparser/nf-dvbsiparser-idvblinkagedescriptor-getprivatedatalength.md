---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetPrivateDataLength
title: IDvbLinkageDescriptor::GetPrivateDataLength method
author: windows-driver-content
description: Gets the length of the private data field from a Digital Video Broadcast (DVB) linkage descriptor.
old-location: mstv\idvblinkagedescriptor_getprivatedatalength.htm
old-project: mstv
ms.assetid: 6c37a877-5a0e-49ed-bf75-bb8ad73fa783
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetPrivateDataLength method [Microsoft TV Technologies], GetPrivateDataLength method [Microsoft TV Technologies], IDvbLinkageDescriptor interface, GetPrivateDataLength,IDvbLinkageDescriptor.GetPrivateDataLength, IDvbLinkageDescriptor, IDvbLinkageDescriptor interface [Microsoft TV Technologies], GetPrivateDataLength method, IDvbLinkageDescriptor::GetPrivateDataLength, dvbsiparser/IDvbLinkageDescriptor::GetPrivateDataLength, mstv.idvblinkagedescriptor_getprivatedatalength
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
-	IDvbLinkageDescriptor.GetPrivateDataLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLinkageDescriptor::GetPrivateDataLength method


## -description


Gets the length of the private data field from a Digital Video Broadcast (DVB) linkage descriptor.


## -parameters




### -param pbVal [out]

Receives the length of the private data field, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4e419b50-b9c2-48e4-a484-f0fcf5c9cb7f">IDvbLinkageDescriptor</a>
 

 

