---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetTag
title: IDvbContentDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag for a Digital Video Broadcast (DVB) content descriptor.
old-location: mstv\idvbcontentdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 3cfbda01-ef69-4b69-90f4-04dd3044ae1f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbContentDescriptor.GetTag, IDvbContentDescriptor::GetTag, dvbsiparser/IDvbContentDescriptor::GetTag, mstv.idvbcontentdescriptor_gettag
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
 - IDvbContentDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbContentDescriptor::GetTag


## -description


Gets the tag for a Digital Video Broadcast (DVB) content descriptor.  


## -parameters




### -param pbVal [out]

Receives the content descriptor tag. For content descriptors, this tag value is "0x54".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7bc74428-f8e3-4d3b-b35a-33e917b18a93">IDvbContentDescriptor</a>
 

 

