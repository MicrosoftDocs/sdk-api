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

# IPersistStream::GetSizeMax


## -description


Retrieves the size of the stream needed to save the object.


## -parameters




### -param pcbSize [out]

The size in bytes of the stream needed to save this object, in bytes.


## -returns



This method returns S_OK to indicate that the size was retrieved successfully.




## -remarks



This method returns the size needed to save an object. You can call this method to determine the size and set the necessary buffers before calling the <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a> method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>GetSizeMax</b> implementation should return a conservative estimate of the necessary size because the caller might call the <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a> method with a non-growable stream.

<h3><a id="URL_Moniker_Notes"></a><a id="url_moniker_notes"></a><a id="URL_MONIKER_NOTES"></a>URL Moniker Notes</h3>
This method retrieves the maximum number of bytes in the stream that will be required by a subsequent call to <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a>. This value is sizeof(ULONG)==4 plus sizeof(WCHAR)*n where n is the length of the full or partial URL string, including the NULL terminator.




## -see-also




<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>
 

 

