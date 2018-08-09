---
UID: NF:objidl.IPersistStream.GetSizeMax
title: IPersistStream::GetSizeMax
author: windows-sdk-content
description: Retrieves the size of the stream needed to save the object.
old-location: com\ipersiststream_getsizemax.htm
old-project: com
ms.assetid: ef9f0afe-b7e5-4b88-b59d-1371ffeaacb8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSizeMax, GetSizeMax method [COM], GetSizeMax method [COM],IPersistStream interface, IPersistStream interface [COM],GetSizeMax method, IPersistStream.GetSizeMax, IPersistStream::GetSizeMax, _com_ipersiststream_getsizemax, com.ipersiststream_getsizemax, objidl/IPersistStream::GetSizeMax
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistStream.GetSizeMax
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

