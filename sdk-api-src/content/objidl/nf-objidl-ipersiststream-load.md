---
UID: NF:objidl.IPersistStream.Load
title: IPersistStream::Load
author: windows-sdk-content
description: Initializes an object from the stream where it was saved previously.
old-location: com\ipersiststream_load.htm
tech.root: com
ms.assetid: 351e1187-9959-4542-8778-925457c3b8e3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPersistStream interface [COM],Load method, IPersistStream.Load, IPersistStream::Load, Load, Load method [COM], Load method [COM],IPersistStream interface, _com_ipersiststream_load, com.ipersiststream_load, objidl/IPersistStream::Load
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistStream.Load
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- objidl.h
: 
- IPersistStream.Load
: 
---

# IPersistStream::Load


## -description


Initializes an object from the stream where it was saved previously.


## -parameters




### -param pStm [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer to the stream from which the object should be loaded.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to lack of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object was not loaded due to some reason other than a lack of memory.

</td>
</tr>
</table>
 




## -remarks



This method loads an object from its associated stream. The seek pointer is set as it was in the most recent <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a> method. This method can seek and read from the stream, but cannot write to it.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Rather than calling <b>IPersistStream::Load</b> directly, you typically call the <a href="https://msdn.microsoft.com/2d54a0ef-906b-4886-a095-4ff2f3d4e634">OleLoadFromStream</a> function does the following:

<ol>
<li>Calls the <a href="https://msdn.microsoft.com/bcf11c5b-e164-4a0f-b30f-ee9e76c4356d">ReadClassStm</a> function to get the class identifier from the stream.</li>
<li>Calls the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function to create an instance of the object.</li>
<li>Queries the instance for <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>.</li>
<li>Calls <b>IPersistStream::Load</b>.</li>
</ol>
The <a href="https://msdn.microsoft.com/2d54a0ef-906b-4886-a095-4ff2f3d4e634">OleLoadFromStream</a> function assumes that objects are stored in the stream with a class identifier followed by the object data. This storage pattern is used by the generic, composite-moniker implementation provided by OLE.

If the objects are not stored using this pattern, you must call the methods separately yourself.


<h3><a id="URL_Moniker_Notes"></a><a id="url_moniker_notes"></a><a id="URL_MONIKER_NOTES"></a>URL Moniker Notes</h3>
Initializes an URL moniker from data within a stream, usually stored there previously using its <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a> (using <a href="https://msdn.microsoft.com/0085c6a8-1a94-4379-9937-c8d792d130da">OleSaveToStream</a>). The binary format of the URL moniker is its URL string in Unicode (may be a full or partial URL string, see <a href="https://msdn.microsoft.com/library/ms775103(v=VS.85).aspx">CreateURLMonikerEx</a> for details). This is represented as a <b>ULONG</b> count of characters followed by that many Unicode characters.




## -see-also




<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>
 

 

