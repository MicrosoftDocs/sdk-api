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

# Metafile::PlayRecord


## -description


The <b>Metafile::PlayRecord</b> method plays a metafile record.


## -parameters




### -param recordType [in]

Type: <b><a href="https://msdn.microsoft.com/520852c1-961e-4deb-9e3a-49ad753fa861">EmfPlusRecordType</a></b>

Element of the <a href="https://msdn.microsoft.com/520852c1-961e-4deb-9e3a-49ad753fa861">EmfPlusRecordType</a> enumeration that specifies the type of metafile record to be played. 


### -param flags [in]

Type: <b>UINT</b>

Set of flags that specify attributes of the record to be played. 


### -param dataSize [in]

Type: <b>UINT</b>

Integer that specifies the number of bytes contained in the record data. 


### -param data [in]

Type: <b>const BYTE*</b>

Pointer to an array of bytes that contains the record data. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



This method is used in conjunction with the <a href="https://msdn.microsoft.com/167a04d5-24f4-4885-b97c-b4536e41e125">EnumerateMetafile Methods</a> method of the 

				<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class. The EnumerateMetafile Methods method calls an application-defined callback function for each record in a specified metafile. The callback function can display each record (or selected records) by calling the <b>Metafile::PlayRecord</b> method.




## -see-also




<a href="https://msdn.microsoft.com/520852c1-961e-4deb-9e3a-49ad753fa861">EmfPlusRecordType</a>



<a href="https://msdn.microsoft.com/167a04d5-24f4-4885-b97c-b4536e41e125">EnumerateMetafile Methods</a>



<a href="https://msdn.microsoft.com/79b8df1b-6fc5-455b-9d08-57d64bf6bffa">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077">Metafiles</a>
 

 

