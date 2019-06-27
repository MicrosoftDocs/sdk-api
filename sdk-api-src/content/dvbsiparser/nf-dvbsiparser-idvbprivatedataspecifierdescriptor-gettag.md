---
UID: NF:dvbsiparser.IDvbPrivateDataSpecifierDescriptor.GetTag
title: IDvbPrivateDataSpecifierDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) private data descriptor.
old-location: mstv\idvbprivatedataspecifierdescriptor_gettag.htm
tech.root: mstv
ms.assetid: bccca68c-d480-47d0-a0db-7a7d3f8376c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbPrivateDataSpecifierDescriptor interface, IDvbPrivateDataSpecifierDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbPrivateDataSpecifierDescriptor.GetTag, IDvbPrivateDataSpecifierDescriptor::GetTag, dvbsiparser/IDvbPrivateDataSpecifierDescriptor::GetTag, mstv.idvbprivatedataspecifierdescriptor_gettag
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDvbPrivateDataSpecifierDescriptor.GetTag"
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
 - IDvbPrivateDataSpecifierDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbPrivateDataSpecifierDescriptor::GetTag


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) private data descriptor. 


## -parameters




### -param pbVal [out]

Receives the private descriptor identifier tag. For private data descriptors, this value is 0x5F.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbprivatedataspecifierdescriptor">IDvbPrivateDataSpecifierDescriptor</a>
 

 

