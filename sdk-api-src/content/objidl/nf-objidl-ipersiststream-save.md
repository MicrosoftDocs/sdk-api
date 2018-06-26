---
UID: NF:objidl.IPersistStream.Save
title: IPersistStream::Save
author: windows-sdk-content
description: Saves an object to the specified stream.
old-location: com\ipersiststream_save.htm
old-project: com
ms.assetid: b748b4f9-ef9c-486b-bdc4-4d23c4640ff7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IPersistStream interface [COM],Save method, IPersistStream.Save, IPersistStream::Save, Save, Save method [COM], Save method [COM],IPersistStream interface, _com_ipersiststream_save, com.ipersiststream_save, objidl/IPersistStream::Save
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
 - IPersistStream.Save
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPersistStream::Save


## -description


Saves an object to the specified stream.


## -parameters




### -param pStm [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer to the stream into which the object should be saved.


### -param fClearDirty [in]

Indicates whether to clear the dirty flag after the save is complete. If <b>TRUE</b>, the flag should be cleared. If <b>FALSE</b>, the flag should be left unchanged.


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
<dt><b>STG_E_CANTSAVE</b></dt>
</dl>
</td>
<td width="60%">
The object could not save itself to the stream. This error could indicate, for example, that the object contains another object that is not serializable to a stream or that an <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> call returned STG_E_CANTSAVE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
The object could not be saved because there is no space left on the storage device.

</td>
</tr>
</table>
 




## -remarks



<b>IPersistStream::Save</b> saves an object into the specified stream and indicates whether the object should reset its dirty flag.

The seek pointer is positioned at the location in the stream at which the object should begin writing its data. The object calls the <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> method to write its data.

On exit, the seek pointer must be positioned immediately past the object data. The position of the seek pointer is undefined if an error returns.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Rather than calling <b>IPersistStream::Save</b> directly, you typically call the <a href="https://msdn.microsoft.com/0085c6a8-1a94-4379-9937-c8d792d130da">OleSaveToStream</a> helper function which does the following: 

<ol>
<li>Calls <a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">GetClassID</a> to get the object's CLSID.</li>
<li>Calls the <a href="https://msdn.microsoft.com/c08bfbc8-f7ac-4534-8c98-c732c6daa2f7">WriteClassStm</a> function to write the object's CLSID to the stream.</li>
<li>Calls <b>IPersistStream::Save</b>.</li>
</ol>
If you call these methods directly, you can write other data into the stream after the CLSID before calling <b>IPersistStream::Save</b>.

The OLE-provided implementation of <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> follows this same pattern.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>IPersistStream::Save</b> method does not write the CLSID to the stream. The caller is responsible for writing the CLSID.

The <b>IPersistStream::Save</b> method can read from, write to, and seek in the stream; but it must not seek to a location in the stream before that of the seek pointer on entry.

<h3><a id="URL_Moniker_Notes"></a><a id="url_moniker_notes"></a><a id="URL_MONIKER_NOTES"></a>URL Moniker Notes</h3>
Saves an URL moniker to a stream. The binary format of URL moniker is its URL string in Unicode (may be a full or partial URL string, see <a href="inet_CreateURLMonikerEx">CreateURLMonikerEx</a> for details). This is represented as a <b>ULONG</b> count of characters followed by that many Unicode characters.




## -see-also




<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>
 

 

