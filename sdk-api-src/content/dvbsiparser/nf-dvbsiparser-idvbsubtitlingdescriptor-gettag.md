---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetTag
title: IDvbSubtitlingDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag for a Digital Video Broadcast (DVB) subtitling descriptor.
old-location: mstv\idvbsubtitlingdescriptor_gettag.htm
tech.root: MSTV
ms.assetid: 2b16b66d-5e71-4204-984d-e9a9d677f4a9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbSubtitlingDescriptor.GetTag, IDvbSubtitlingDescriptor::GetTag, dvbsiparser/IDvbSubtitlingDescriptor::GetTag, mstv.idvbsubtitlingdescriptor_gettag
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
 - IDvbSubtitlingDescriptor.GetTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSubtitlingDescriptor::GetTag


## -description


Gets the tag for a Digital Video Broadcast (DVB) subtitling descriptor. 


## -parameters




### -param pbVal [out]

Receives the subtitling descriptor tag. For subtitling descriptors, this tag value is "0x59". 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7308e8a9-6e16-4719-b87e-9445499f499c">IDvbSubtitlingDescriptor</a>
 

 

