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

# ILockBytes::WriteAt


## -description


The <b>WriteAt</b> method writes the specified number of bytes starting at a specified offset from the beginning of the byte array.


## -parameters




### -param ulOffset [in]

Specifies the starting point from the beginning of the byte array for the data to be written.


### -param pv [in]

Pointer to the buffer containing the data to be written.


### -param cb [in]

Specifies the number of bytes of data to attempt to write into the byte array.


### -param pcbWritten [out]

Pointer to a location where this method specifies the actual number of bytes written to the byte array. You can set this pointer to <b>NULL</b> to indicate that you are not interested in this value. In this case, this method does not provide the actual number of bytes written.


## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::WriteAt</b> writes the specified data at the specified location in the byte array. The number of bytes actually written must always be returned in <i>pcbWritten</i>, even if an error is returned. If the byte count is zero bytes, the write operation has no effect.

If <i>ulOffset</i> is past the end of the byte array and <i>cb</i> is greater than zero, <b>ILockBytes::WriteAt</b> increases the size of the byte array. The fill bytes written to the byte array are not initialized to any particular value.




## -see-also




<a href="https://msdn.microsoft.com/700b6a3c-1046-4c21-8887-16f344c23510">ILockBytes - File-Based Implementation</a>



<a href="https://msdn.microsoft.com/6ab019b0-34d7-4b6e-ba77-6b6881fabd29">ILockBytes - Global Memory Implementation</a>



<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a>



<a href="https://msdn.microsoft.com/13b3237b-d113-4505-b397-b06916368fef">ILockBytes::SetSize</a>
 

 

