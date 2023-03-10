---
UID: NF:ocidl.IPersistStreamInit.IsDirty
title: IPersistStreamInit::IsDirty (ocidl.h)
description: Determines whether an object has changed since it was last saved to its stream. (IPersistStreamInit.IsDirty)
helpviewer_keywords: ["IPersistStreamInit interface [COM]","IsDirty method","IPersistStreamInit.IsDirty","IPersistStreamInit::IsDirty","IsDirty","IsDirty method [COM]","IsDirty method [COM]","IPersistStreamInit interface","_com_ipersiststreaminit_isdirty","com.ipersiststreaminit_isdirty","ocidl/IPersistStreamInit::IsDirty"]
old-location: com\ipersiststreaminit_isdirty.htm
tech.root: com
ms.assetid: 2b84818d-0d9d-4f55-8031-b4336baa6c09
ms.date: 12/05/2018
ms.keywords: IPersistStreamInit interface [COM],IsDirty method, IPersistStreamInit.IsDirty, IPersistStreamInit::IsDirty, IsDirty, IsDirty method [COM], IsDirty method [COM],IPersistStreamInit interface, _com_ipersiststreaminit_isdirty, com.ipersiststreaminit_isdirty, ocidl/IPersistStreamInit::IsDirty
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
 - IPersistStreamInit::IsDirty
 - ocidl/IPersistStreamInit::IsDirty
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
 - IPersistStreamInit.IsDirty
---

# IPersistStreamInit::IsDirty


## -description

Determines whether an object has changed since it was last saved to its stream.



## -returns

This method returns S_OK to indicate that the object has changed. Otherwise, it returns S_FALSE.

## -remarks

Use this method to determine whether an object should be saved before closing it. The dirty flag for an object is conditionally cleared in the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-save">IPersistStreamInit::Save</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You should treat any error return codes as an indication that the object has changed. Unless this method explicitly returns S_FALSE, assume that the object must be saved.

Note that the OLE-provided implementations of the <b>IPersistStreamInit::IsDirty</b> method in the OLE-provided moniker interfaces always return S_FALSE because their internal state never changes.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>
