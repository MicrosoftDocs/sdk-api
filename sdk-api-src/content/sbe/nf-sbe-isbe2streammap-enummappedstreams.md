---
UID: NF:sbe.ISBE2StreamMap.EnumMappedStreams
title: ISBE2StreamMap::EnumMappedStreams
author: windows-driver-content
description: Enumerates streams that are mapped to output pins in a Stream Buffer Source filter.
old-location: mstv\isbe2streammap_enummappedstreams.htm
old-project: mstv
ms.assetid: bb98db94-3aa1-4f29-b98a-7594e27466ef
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: EnumMappedStreams, EnumMappedStreams method [Microsoft TV Technologies], EnumMappedStreams method [Microsoft TV Technologies],ISBE2StreamMap interface, ISBE2StreamMap interface [Microsoft TV Technologies],EnumMappedStreams method, ISBE2StreamMap.EnumMappedStreams, ISBE2StreamMap::EnumMappedStreams, mstv.isbe2streammap_enummappedstreams, sbe/ISBE2StreamMap::EnumMappedStreams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbe.h
api_name:
-	ISBE2StreamMap.EnumMappedStreams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISBE2StreamMap::EnumMappedStreams


## -description


Enumerates streams that are mapped to output pins in a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter.


## -parameters




### -param ppStreams [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a> interface for an enumeration object that lists all streams mapped to the filter outputs pin.
          The caller is responsible for freeing the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Windows 7, only one stream at a time can be mapped to an output pin, although a call to the <a href="https://msdn.microsoft.com/efe3b21d-9664-4367-9bfe-4c02589370c4">ISBE2StreamMap::MapStream</a> method can be used to change the stream mapped to any particular pin while the graph is running. In previous versions of Windows, a stream mapped to a pin could not be changed while the graph was running.




## -see-also




<a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a>



<a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a>



<a href="https://msdn.microsoft.com/d63691ca-2420-4c54-b343-be85d634488c">ISBE2StreamMap</a>



<a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source Filter</a>
 

 

