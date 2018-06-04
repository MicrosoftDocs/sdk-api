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

# IMPEG2ComponentType::put_StreamType


## -description



The <b>put_StreamType</b> method sets the MPEG2 stream type.




## -parameters




### -param MP2StreamType [in]

Variable of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff567738">MPEG2StreamType</a> that specifies the stream type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/10bf35e0-d5bf-41ed-b514-7c1bfaf774a0">IMPEG2ComponentType Interface</a>
 

 

