---
UID: NF:ocidl.IPersistStreamInit.Save
title: IPersistStreamInit::Save method
author: windows-driver-content
description: Saves an object to the specified stream.
old-location: com\ipersiststreaminit_save.htm
old-project: com
ms.assetid: f88b61d0-dd85-4e8e-b445-dfced6521981
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IPersistStreamInit, IPersistStreamInit interface [COM], Save method, IPersistStreamInit::Save, Save method [COM], Save method [COM], IPersistStreamInit interface, Save,IPersistStreamInit.Save, _com_ipersiststreaminit_save, com.ipersiststreaminit_save, ocidl/IPersistStreamInit::Save
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPersistStreamInit.Save
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPersistStreamInit::Save method


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



<b>IPersistStreamInit::Save</b> saves an object into the specified stream and indicates whether the object should reset its dirty flag.

The seek pointer is positioned at the location in the stream at which the object should begin writing its data. The object calls the <a href="https://msdn.microsoft.com/f0323dda-6c31-4411-bf20-9650162109c0">ISequentialStream::Write</a> method to write its data.

On exit, the seek pointer must be positioned immediately past the object data. The position of the seek pointer is undefined if an error returns.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>IPersistStreamInit::Save</b> method does not write the CLSID to the stream. The caller is responsible for writing the CLSID.

The <b>IPersistStreamInit::Save</b> method can read from, write to, and seek in the stream; but it must not seek to a location in the stream before that of the seek pointer on entry.




## -see-also




<a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a>
 

 

