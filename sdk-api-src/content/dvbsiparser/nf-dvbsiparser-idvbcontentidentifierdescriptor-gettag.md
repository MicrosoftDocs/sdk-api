---
UID: NF:dvbsiparser.IDvbContentIdentifierDescriptor.GetTag
title: IDvbContentIdentifierDescriptor::GetTag method
author: windows-driver-content
description: Gets the tag for a Digital Video Broadcast (DVB) content identifier descriptor.
old-location: mstv\idvbcontentidentifierdescriptor_gettag.htm
old-project: mstv
ms.assetid: 0ab8dbe8-ddb8-4c24-a830-c770eab2b23f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies], IDvbContentIdentifierDescriptor interface, GetTag,IDvbContentIdentifierDescriptor.GetTag, IDvbContentIdentifierDescriptor, IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies], GetTag method, IDvbContentIdentifierDescriptor::GetTag, dvbsiparser/IDvbContentIdentifierDescriptor::GetTag, mstv.idvbcontentidentifierdescriptor_gettag
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
-	IDvbContentIdentifierDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbContentIdentifierDescriptor::GetTag method


## -description


Gets the tag for a Digital Video Broadcast (DVB) content identifier descriptor.  


## -parameters




### -param pbVal [out]

Receives the content identifier descriptor tag. For content identifier descriptors, this tag value is "0x76". 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bdd15b6f-2f1e-438a-a2fd-f3fa4df2a9fd">IDvbContentIdentifierDescriptor</a>
 

 

