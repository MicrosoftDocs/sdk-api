---
UID: NF:ocidl.IPersistStreamInit.Save
title: IPersistStreamInit::Save (ocidl.h)
description: Saves an object to the specified stream. (IPersistStreamInit.Save)
helpviewer_keywords: ["IPersistStreamInit interface [COM]","Save method","IPersistStreamInit.Save","IPersistStreamInit::Save","Save","Save method [COM]","Save method [COM]","IPersistStreamInit interface","_com_ipersiststreaminit_save","com.ipersiststreaminit_save","ocidl/IPersistStreamInit::Save"]
old-location: com\ipersiststreaminit_save.htm
tech.root: com
ms.assetid: f88b61d0-dd85-4e8e-b445-dfced6521981
ms.date: 12/05/2018
ms.keywords: IPersistStreamInit interface [COM],Save method, IPersistStreamInit.Save, IPersistStreamInit::Save, Save, Save method [COM], Save method [COM],IPersistStreamInit interface, _com_ipersiststreaminit_save, com.ipersiststreaminit_save, ocidl/IPersistStreamInit::Save
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IPersistStreamInit::Save
 - ocidl/IPersistStreamInit::Save
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPersistStreamInit.Save
---

# IPersistStreamInit::Save


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

<b>IPersistStreamInit::Save</b> saves an object into the specified stream and indicates whether the object should reset its dirty flag.

The seek pointer is positioned at the location in the stream at which the object should begin writing its data. The object calls the <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> method to write its data.

On exit, the seek pointer must be positioned immediately past the object data. The position of the seek pointer is undefined if an error returns.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>IPersistStreamInit::Save</b> method does not write the CLSID to the stream. The caller is responsible for writing the CLSID.

The <b>IPersistStreamInit::Save</b> method can read from, write to, and seek in the stream; but it must not seek to a location in the stream before that of the seek pointer on entry.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>
