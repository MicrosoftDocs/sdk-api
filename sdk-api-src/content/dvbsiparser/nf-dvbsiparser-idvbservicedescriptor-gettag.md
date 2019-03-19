---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetTag
title: IDvbServiceDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag identifying a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 0cdf6279-3156-43eb-97e3-58a4f9d93cc6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbServiceDescriptor.GetTag, IDvbServiceDescriptor::GetTag, dvbsiparser/IDvbServiceDescriptor::GetTag, mstv.idvbservicedescriptor_gettag
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
 - IDvbServiceDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbServiceDescriptor::GetTag


## -description


Gets the tag identifying a Digital Video Broadcast (DVB) service descriptor. 


## -parameters




### -param pbVal [out]

Receives the service descriptor tag. This value is 0x48 for service descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7024259f-3dcf-46e0-9984-d5924c9e5b54">IDvbServiceDescriptor</a>
 

 

