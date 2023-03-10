---
UID: NF:objidl.IPersistStream.IsDirty
title: IPersistStream::IsDirty (objidl.h)
description: Determines whether an object has changed since it was last saved to its stream. (IPersistStream.IsDirty)
helpviewer_keywords: ["IPersistStream interface [COM]","IsDirty method","IPersistStream.IsDirty","IPersistStream::IsDirty","IsDirty","IsDirty method [COM]","IsDirty method [COM]","IPersistStream interface","_com_ipersiststream_isdirty","com.ipersiststream_isdirty","objidl/IPersistStream::IsDirty"]
old-location: com\ipersiststream_isdirty.htm
tech.root: com
ms.assetid: fabafc37-18f2-4def-b6bf-f7daa2bb8f37
ms.date: 12/05/2018
ms.keywords: IPersistStream interface [COM],IsDirty method, IPersistStream.IsDirty, IPersistStream::IsDirty, IsDirty, IsDirty method [COM], IsDirty method [COM],IPersistStream interface, _com_ipersiststream_isdirty, com.ipersiststream_isdirty, objidl/IPersistStream::IsDirty
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
 - IPersistStream::IsDirty
 - objidl/IPersistStream::IsDirty
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
 - IPersistStream.IsDirty
---

# IPersistStream::IsDirty


## -description

Determines whether an object has changed since it was last saved to its stream.



## -returns

This method returns S_OK to indicate that the object has changed. Otherwise, it returns S_FALSE.

## -remarks

Use this method to determine whether an object should be saved before closing it. The dirty flag for an object is conditionally cleared in the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-save">IPersistStream::Save</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You should treat any error return codes as an indication that the object has changed. Unless this method explicitly returns S_FALSE, assume that the object must be saved.

Note that the OLE-provided implementations of the <b>IPersistStream::IsDirty</b> method in the OLE-provided moniker interfaces always return S_FALSE because their internal state never changes.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>
