---
UID: NF:dvbsiparser.IDvbPrivateDataSpecifierDescriptor.GetTag
title: IDvbPrivateDataSpecifierDescriptor::GetTag method
author: windows-driver-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) private data descriptor.
old-location: mstv\idvbprivatedataspecifierdescriptor_gettag.htm
old-project: mstv
ms.assetid: bccca68c-d480-47d0-a0db-7a7d3f8376c2
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies], IDvbPrivateDataSpecifierDescriptor interface, GetTag,IDvbPrivateDataSpecifierDescriptor.GetTag, IDvbPrivateDataSpecifierDescriptor, IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies], GetTag method, IDvbPrivateDataSpecifierDescriptor::GetTag, dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetTag, mstv.idvbprivatedataspecifierdescriptor_gettag
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbPrivateDataSpecifierDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbPrivateDataSpecifierDescriptor::GetTag method


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) private data descriptor. 


## -parameters




### -param pbVal [out]

Receives the private descriptor identifier tag. For private data descriptors, this value is 0x5F.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d5a78a3-0d56-47e8-939f-006d5f4db5c4">IDvbPrivateDataSpecifierDescriptor</a>
 

 

