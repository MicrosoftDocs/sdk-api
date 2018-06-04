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

# IWMWriterFileSink3::OnDataUnitEx


## -description



The <b>OnDataUnitEx</b> method is called when the writer has finished sending a data unit.



<b>OnDataUnitEx</b> is an enhanced version of <a href="https://msdn.microsoft.com/32e52cdb-e7cb-4caf-a202-0d2ff746017c">IWMWriterSink::OnDataUnit</a>. The difference between these two methods is that <b>OnDataUnitEx</b> delivers very granular data unit information. You can examine individual payload headers, payload data fragments, and the packet header.


## -parameters




### -param pFileSinkDataUnit [in]

Pointer to a <a href="https://msdn.microsoft.com/e1deb01f-9f53-4ede-a3e1-13d6dc79adb5">WMT_FILESINK_DATA_UNIT</a> structure containing the data unit information.


## -returns



This method always returns S_OK.




## -remarks



Applications do not call this method. If you are implementing the <b>IWMWriterFileSink3</b> interface on a custom sink, you have the option of implementing this method. If you do so, your implementation of <a href="https://msdn.microsoft.com/a8a7003e-e59f-451c-9f45-75d6d094a03b">GetMode</a> should return WMT_FM_FILESINK_DATA_UNITS.




## -see-also




<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>
 

 

