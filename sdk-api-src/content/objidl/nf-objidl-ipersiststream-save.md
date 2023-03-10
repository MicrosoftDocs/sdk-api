---
UID: NF:objidl.IPersistStream.Save
title: IPersistStream::Save (objidl.h)
description: Saves an object to the specified stream. (IPersistStream.Save)
helpviewer_keywords: ["IPersistStream interface [COM]","Save method","IPersistStream.Save","IPersistStream::Save","Save","Save method [COM]","Save method [COM]","IPersistStream interface","_com_ipersiststream_save","com.ipersiststream_save","objidl/IPersistStream::Save"]
old-location: com\ipersiststream_save.htm
tech.root: com
ms.assetid: b748b4f9-ef9c-486b-bdc4-4d23c4640ff7
ms.date: 12/05/2018
ms.keywords: IPersistStream interface [COM],Save method, IPersistStream.Save, IPersistStream::Save, Save, Save method [COM], Save method [COM],IPersistStream interface, _com_ipersiststream_save, com.ipersiststream_save, objidl/IPersistStream::Save
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistStream::Save
 - objidl/IPersistStream::Save
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistStream.Save
---

# IPersistStream::Save


## -description

Saves an object to the specified stream.

## -parameters

### -param pStm [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer to the stream into which the object should be saved.

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
The object could not save itself to the stream. This error could indicate, for example, that the object contains another object that is not serializable to a stream or that an <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> call returned STG_E_CANTSAVE.

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

The seek pointer is positioned at the location in the stream at which the object should begin writing its data. The object calls the <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> method to write its data.

On exit, the seek pointer must be positioned immediately past the object data. The position of the seek pointer is undefined if an error returns.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Rather than calling <b>IPersistStream::Save</b> directly, you typically call the <a href="/windows/desktop/api/ole/nf-ole-olesavetostream">OleSaveToStream</a> helper function which does the following: 

<ol>
<li>Calls <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">GetClassID</a> to get the object's CLSID.</li>
<li>Calls the <a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstm">WriteClassStm</a> function to write the object's CLSID to the stream.</li>
<li>Calls <b>IPersistStream::Save</b>.</li>
</ol>
If you call these methods directly, you can write other data into the stream after the CLSID before calling <b>IPersistStream::Save</b>.

The OLE-provided implementation of <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> follows this same pattern.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>IPersistStream::Save</b> method does not write the CLSID to the stream. The caller is responsible for writing the CLSID.

The <b>IPersistStream::Save</b> method can read from, write to, and seek in the stream; but it must not seek to a location in the stream before that of the seek pointer on entry.

<h3><a id="URL_Moniker_Notes"></a><a id="url_moniker_notes"></a><a id="URL_MONIKER_NOTES"></a>URL Moniker Notes</h3>
Saves an URL moniker to a stream. The binary format of URL moniker is its URL string in Unicode (may be a full or partial URL string, see <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775103(v=vs.85)">CreateURLMonikerEx</a> for details). This is represented as a <b>ULONG</b> count of characters followed by that many Unicode characters.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>
