---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetTag
title: IDvbServiceListDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag identifying a Digital Video Broadcast (DVB) service list descriptor.
old-location: mstv\idvbservicelistdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 5e16ab7f-25df-461e-b3aa-73de613e45b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbServiceListDescriptor.GetTag, IDvbServiceListDescriptor::GetTag, dvbsiparser/IDvbServiceListDescriptor::GetTag, mstv.idvbservicelistdescriptor_gettag
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
 - IDvbServiceListDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbServiceListDescriptor::GetTag


## -description


Gets the tag identifying a Digital Video Broadcast (DVB) service list descriptor. 


## -parameters




### -param pbVal [out]

Receives the service list descriptor tag. Typically, this value is 0x41 for service list descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d39595b-0297-473d-9b0f-e038a938a196">IDvbServiceListDescriptor</a>
 

 

