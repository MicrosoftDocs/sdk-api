---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetTag
title: IDvbMultilingualServiceNameDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag identifying a Digital Video Broadcast (DVB) multilingual service name descriptor.
old-location: mstv\idvbmultilingualservicenamedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 428f3309-67aa-4a47-9585-0308bee47e16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbMultilingualServiceNameDescriptor interface, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbMultilingualServiceNameDescriptor.GetTag, IDvbMultilingualServiceNameDescriptor::GetTag, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetTag, mstv.idvbmultilingualservicenamedescriptor_gettag
ms.topic: method
f1_keywords: ["dvbsiparser/IDvbMultilingualServiceNameDescriptor.GetTag"]
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
 - IDvbMultilingualServiceNameDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbMultilingualServiceNameDescriptor::GetTag


## -description


Gets the tag identifying a Digital Video Broadcast (DVB) multilingual service name descriptor. 


## -parameters




### -param pbVal [out]

Receives the service list descriptor tag. Typically, this value is 0x5D for multilingual service name descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbmultilingualservicenamedescriptor">IDvbMultilingualServiceNameDescriptor</a>
 

 

