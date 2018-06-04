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

# IAudioProcessingObjectRT::APOProcess


## -description


The APOProcess method causes the APO to make a processing pass.


## -parameters




### -param u32NumInputConnections [in]

The number of input connections that are attached to this APO.


### -param ppInputConnections [in]

An array of input connection property structures. There is one structure per input connection.


### -param u32NumOutputConnections [in]

The number of output connections that are attached to this APO.


### -param ppOutputConnections [in, out]

An array of output connection property structures. There is one structure per output connection.


## -returns



None

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
</table>
 




## -remarks



The <code>APOProcess</code> method must not change the data in the ppOutputConnections array. But it must set the properties of the output connections after processing.

The <code>APOProcess</code> method is called from a real-time processing thread. The implementation of this method must not touch paged memory and it should not call any system blocking routines.

For a detailed look at an implementation of this method, see the <a href="https://msdn.microsoft.com/bafbc56c-53a3-41a5-b077-3289967daf87">Swap sample code</a> and refer to the Swapapolfx.cpp file.




## -see-also




<a href="https://msdn.microsoft.com/bafbc56c-53a3-41a5-b077-3289967daf87">Swap sample code</a>
 

 

