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

# WTSVirtualChannelWrite function


## -description


Writes 
    data to the server end of a virtual channel.


## -parameters




### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
      <a href="https://msdn.microsoft.com/0daaf06f-ba05-469c-b888-3df5d9495364">WTSVirtualChannelOpen</a> function.


### -param Buffer [in]

Pointer to a buffer containing the data to write to the virtual channel.


### -param Length [in]

Specifies the size, in bytes, of the data to write.


### -param pBytesWritten [out]

Pointer to a variable that receives the number of bytes written.


## -returns



If the function succeeds, the return value is a nonzero value.


       If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
      




## -remarks



<div class="alert"><b>Note</b>  <b>WTSVirtualChannelWrite</b> is not thread safe. 
    To access a virtual channel from multiple threads, or to do asynchronous IO through a virtual channel, use 
    <a href="https://msdn.microsoft.com/68ae8174-d72b-4b1c-b8e9-ae5fed51d385">WTSVirtualChannelQuery</a> with 
    <b>WTSVirtualFileHandle</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/68ae8174-d72b-4b1c-b8e9-ae5fed51d385">WTSVirtualChannelQuery</a>



<a href="https://msdn.microsoft.com/7434e761-303f-496f-81cb-83c199ddec8a">WTSVirtualChannelRead</a>
 

 

