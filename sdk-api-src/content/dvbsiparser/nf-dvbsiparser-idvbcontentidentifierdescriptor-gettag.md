---
UID: NF:dvbsiparser.IDvbContentIdentifierDescriptor.GetTag
title: IDvbContentIdentifierDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag for a Digital Video Broadcast (DVB) content identifier descriptor.
old-location: mstv\idvbcontentidentifierdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 0ab8dbe8-ddb8-4c24-a830-c770eab2b23f
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbContentIdentifierDescriptor interface, IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbContentIdentifierDescriptor.GetTag, IDvbContentIdentifierDescriptor::GetTag, dvbsiparser/IDvbContentIdentifierDescriptor::GetTag, mstv.idvbcontentidentifierdescriptor_gettag
ms.topic: method
f1_keywords:
- dvbsiparser/IDvbContentIdentifierDescriptor.GetTag
dev_langs:
- c++
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
- IDvbContentIdentifierDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbContentIdentifierDescriptor::GetTag


## -description


Gets the tag for a Digital Video Broadcast (DVB) content identifier descriptor.  


## -parameters




### -param pbVal [out]

Receives the content identifier descriptor tag. For content identifier descriptors, this tag value is "0x76". 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentidentifierdescriptor">IDvbContentIdentifierDescriptor</a>
 

 

