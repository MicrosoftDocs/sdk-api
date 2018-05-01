---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetTag
title: IDvbLinkageDescriptor::GetTag method
author: windows-driver-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) linkage descriptor.
old-location: mstv\idvblinkagedescriptor_gettag.htm
old-project: mstv
ms.assetid: 4a01430f-13b2-40ff-a47e-98e1bcdbf4fc
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies], IDvbLinkageDescriptor interface, GetTag,IDvbLinkageDescriptor.GetTag, IDvbLinkageDescriptor, IDvbLinkageDescriptor interface [Microsoft TV Technologies], GetTag method, IDvbLinkageDescriptor::GetTag, dvbsiparser/IDvbLinkageDescriptor::GetTag, mstv.idvblinkagedescriptor_gettag
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
-	IDvbLinkageDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLinkageDescriptor::GetTag method


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) linkage descriptor.


## -parameters




### -param pbVal [out]

Receives the identifier tag. For DVB linkage descriptors, this value is "0x4A".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4e419b50-b9c2-48e4-a484-f0fcf5c9cb7f">IDvbLinkageDescriptor</a>
 

 

