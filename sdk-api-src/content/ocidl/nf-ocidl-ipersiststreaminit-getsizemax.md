---
UID: NF:ocidl.IPersistStreamInit.GetSizeMax
title: IPersistStreamInit::GetSizeMax (ocidl.h)
description: Retrieves the size of the stream needed to save the object. (IPersistStreamInit.GetSizeMax)
helpviewer_keywords: ["GetSizeMax","GetSizeMax method [COM]","GetSizeMax method [COM]","IPersistStreamInit interface","IPersistStreamInit interface [COM]","GetSizeMax method","IPersistStreamInit.GetSizeMax","IPersistStreamInit::GetSizeMax","_com_ipersiststreaminit_getsizemax","com.ipersiststreaminit_getsizemax","ocidl/IPersistStreamInit::GetSizeMax"]
old-location: com\ipersiststreaminit_getsizemax.htm
tech.root: com
ms.assetid: 8413eeda-3867-4352-aefb-82579a4861f2
ms.date: 12/05/2018
ms.keywords: GetSizeMax, GetSizeMax method [COM], GetSizeMax method [COM],IPersistStreamInit interface, IPersistStreamInit interface [COM],GetSizeMax method, IPersistStreamInit.GetSizeMax, IPersistStreamInit::GetSizeMax, _com_ipersiststreaminit_getsizemax, com.ipersiststreaminit_getsizemax, ocidl/IPersistStreamInit::GetSizeMax
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
 - IPersistStreamInit::GetSizeMax
 - ocidl/IPersistStreamInit::GetSizeMax
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
 - IPersistStreamInit.GetSizeMax
---

# IPersistStreamInit::GetSizeMax


## -description

Retrieves the size of the stream needed to save the object.

## -parameters

### -param pCbSize [out]

The size in bytes of the stream needed to save this object, in bytes.

## -returns

This method returns S_OK to indicate that the size was retrieved successfully.

## -remarks

This method returns the size needed to save an object. You can call this method to determine the size and set the necessary buffers before calling the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-save">IPersistStreamInit::Save</a> method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>GetSizeMax</b> implementation should return a conservative estimate of the necessary size because the caller might call the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-save">IPersistStreamInit::Save</a> method with a non-growable stream.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>
