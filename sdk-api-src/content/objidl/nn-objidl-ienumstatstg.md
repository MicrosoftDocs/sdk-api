---
UID: NN:objidl.IEnumSTATSTG
title: IEnumSTATSTG (objidl.h)
description: Enumerates an array of STATSTG structures.
helpviewer_keywords: ["IEnumSTATSTG","IEnumSTATSTG interface [Structured Storage]","IEnumSTATSTG interface [Structured Storage]","described","_stg_ienumstatstg","objidl/IEnumSTATSTG","stg.ienumstatstg"]
old-location: stg\ienumstatstg.htm
tech.root: Stg
ms.assetid: 93b8b14e-94e4-460b-9846-413affad8e4f
ms.date: 12/05/2018
ms.keywords: IEnumSTATSTG, IEnumSTATSTG interface [Structured Storage], IEnumSTATSTG interface [Structured Storage],described, _stg_ienumstatstg, objidl/IEnumSTATSTG, stg.ienumstatstg
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumSTATSTG
 - objidl/IEnumSTATSTG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATSTG
---

# IEnumSTATSTG interface


## -description

The 
<b>IEnumSTATSTG</b> interface enumerates an array of 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structures. These structures contain statistical data about  open storage, stream, or byte array objects. 
<b>IEnumSTATSTG</b> has the same methods as all enumerator interfaces: <a href="/windows/desktop/api/objidl/nf-objidl-ienumstatstg-next">Next</a>, <a href="/windows/desktop/api/objidl/nf-objidl-ienumstatstg-skip">Skip</a>, <a href="/windows/desktop/api/objidl/nf-objidl-ienumstatstg-reset">Reset</a>, and 
<a href="/windows/desktop/api/objidl/nf-objidl-ienumstatstg-clone">Clone</a>.

## -inheritance

The <b>IEnumSTATSTG</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSTATSTG</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>



<a href="/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-enumelements">IStorage::EnumElements</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>
