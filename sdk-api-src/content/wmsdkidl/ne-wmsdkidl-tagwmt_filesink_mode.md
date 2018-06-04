---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagWMT_FILESINK_MODE enumeration


## -description



The <b>WMT_FILESINK_MODE</b> enumeration type defines the types of input accepted by the file sink.




## -enum-fields




### -field WMT_FM_SINGLE_BUFFERS

The file sink accepts normal buffers through calls to <a href="https://msdn.microsoft.com/32e52cdb-e7cb-4caf-a202-0d2ff746017c">IWMWriterSink::OnDataUnit</a>. This is the default behavior.


### -field WMT_FM_FILESINK_DATA_UNITS

The file sink accepts data as <a href="https://msdn.microsoft.com/e1deb01f-9f53-4ede-a3e1-13d6dc79adb5">WMT_FILESINK_DATA_UNIT</a> structures delivered by <a href="https://msdn.microsoft.com/1dbcb27b-7588-4475-99fe-3e547d1659d3">IWMWriterFileSink3::OnDataUnitEx</a>.


### -field WMT_FM_FILESINK_UNBUFFERED

The file sink accepts unbuffered data. A call to <a href="https://msdn.microsoft.com/51a9c21b-d301-41e4-a9bc-321a5b2decca">IWMWriterFileSink3::SetUnbufferedIO</a> will succeed.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

