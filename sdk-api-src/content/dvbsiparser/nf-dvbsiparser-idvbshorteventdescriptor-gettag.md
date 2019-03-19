---
UID: NF:dvbsiparser.IDvbShortEventDescriptor.GetTag
title: IDvbShortEventDescriptor::GetTag (dvbsiparser.h)
author: windows-sdk-content
description: Gets the tag that identifies a Digital Video Broadcast (DVB) short event descriptor.
old-location: mstv\idvbshorteventdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 4cf7a327-6646-4cea-95ab-125450f013b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbShortEventDescriptor interface, IDvbShortEventDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbShortEventDescriptor.GetTag, IDvbShortEventDescriptor::GetTag, dvbsiparser/IDvbShortEventDescriptor::GetTag, mstv.idvbshorteventdescriptor_gettag
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
 - IDvbShortEventDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbShortEventDescriptor::GetTag


## -description


Gets the tag that identifies a Digital Video Broadcast (DVB) short event  descriptor.


## -parameters




### -param pbVal [out]

Receives the identifier tag. For DVB short event descriptors, this value is "0x4D".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/039ae2e1-1dad-4a70-a054-bd95b0b500fb">IDvbShortEventDescriptor</a>
 

 

