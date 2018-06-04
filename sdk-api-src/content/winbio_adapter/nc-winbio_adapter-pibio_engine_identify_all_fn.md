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

# PIBIO_ENGINE_IDENTIFY_ALL_FN callback function


## -description


Called by the Windows Biometric Framework to determine the identities of any people who are currently in camera frame.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param PresenceCount [out]

Address of a variable that receives the number of presences detected by the function.


### -param *PresenceArray [out]

Address of a variable that receives a pointer to an array of <a href="https://msdn.microsoft.com/810D452E-DDFA-4AB2-AEFB-0C170C0C18D4">WINBIO_PRESENCE</a> elements.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_some_error </b></dt>
</dl>
</td>
<td width="60%">
Any error code will cause the Biometric Service to log the error and ignore the camera frame.

</td>
</tr>
</table>
 




## -remarks



The biometric service calls this method after it sends a new frame of data to the engine adapter.

After processing the data frame, this function should return one <a href="https://msdn.microsoft.com/810D452E-DDFA-4AB2-AEFB-0C170C0C18D4">WINBIO_PRESENCE</a> element for each presence detected in the data frame.

In the event that the <b>EngineAdapterIdentifyAll</b> function can’t find any faces in frame, it returns an <b>HRESULT</b> of <b>S_OK</b> and sets the <i>PresenceCount</i> and <i>PresenceArray</i> return parameters to zero and <b>NULL</b>, respectively. In other words, a frame that doesn’t contain any human presences is not an error condition. 

The only time <b>EngineAdapterIdentifyAll</b> should return an <b>HRESULT</b> other than <b>S_OK</b> is if it doesn’t want the bio service to use the frame to update the Presence Monitor state. This should be a rare occurrence.
The engine adapter is responsible for allocating the array of <a href="https://msdn.microsoft.com/810D452E-DDFA-4AB2-AEFB-0C170C0C18D4">WINBIO_PRESENCE</a> elements it returns in the <i>PresenceArray</i> parameter. It must allocate this memory from the process heap by using the <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> function. After the array is created, it becomes the property of the Windows Biometric Framework. Because the Framework deallocates this memory after using it, your engine adapter must not attempt to deallocate the array or save a pointer to it. Failure to follow this rule will lead to heap corruption and possible crashes of the biometric service.


The values of the individual <a href="https://msdn.microsoft.com/810D452E-DDFA-4AB2-AEFB-0C170C0C18D4">WINBIO_PRESENCE</a> items in the <i>PresenceArray</i> will determine the events generated for client applications. See the discussion of the <b>WINBIO_PRESENCE</b> structure for details.



