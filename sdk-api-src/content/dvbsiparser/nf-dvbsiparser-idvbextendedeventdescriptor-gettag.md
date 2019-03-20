---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetTag
title: IDvbExtendedEventDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) extended event descriptor.
old-location: mstv\idvbextendedeventdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 8f6dad8a-fd95-48c3-9bb2-222c5ec958f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbExtendedEventDescriptor.GetTag, IDvbExtendedEventDescriptor::GetTag, dvbsiparser/IDvbExtendedEventDescriptor::GetTag, mstv.idvbextendedeventdescriptor_gettag
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
 - IDvbExtendedEventDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbExtendedEventDescriptor::GetTag


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) extended event  descriptor.


## -parameters




### -param pbVal [out]

Receives the identifier tag. For DVB  extended event descriptors, this value is "0x4E".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/db100f17-f7b8-4252-8090-44567ab9dcbe">IDvbExtendedEventDescriptor</a>
 

 

