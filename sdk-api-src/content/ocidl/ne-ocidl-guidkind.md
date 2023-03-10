---
UID: NE:ocidl.tagGUIDKIND
title: GUIDKIND (ocidl.h)
description: Flags used to specify the kind of information requested from an object in the IProvideClassInfo2.
helpviewer_keywords: ["GUIDKIND","GUIDKIND enumeration [COM]","GUIDKIND_DEFAULT_SOURCE_DISP_IID","_ctrl_GUIDKIND","com.guidkind","ocidl/GUIDKIND","ocidl/GUIDKIND_DEFAULT_SOURCE_DISP_IID"]
old-location: com\guidkind.htm
tech.root: com
ms.assetid: b9ddd96b-0418-4e31-aaf9-ca060c405fa7
ms.date: 12/05/2018
ms.keywords: GUIDKIND, GUIDKIND enumeration [COM], GUIDKIND_DEFAULT_SOURCE_DISP_IID, _ctrl_GUIDKIND, com.guidkind, ocidl/GUIDKIND, ocidl/GUIDKIND_DEFAULT_SOURCE_DISP_IID
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GUIDKIND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagGUIDKIND
 - ocidl/tagGUIDKIND
 - GUIDKIND
 - ocidl/GUIDKIND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - GUIDKIND
---

# GUIDKIND enumeration


## -description

Flags used to specify the kind of information requested from an object in the <a href="/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo2">IProvideClassInfo2</a>.

## -enum-fields

### -field GUIDKIND_DEFAULT_SOURCE_DISP_IID:1

The interface identifier (IID) of the object's outgoing dispinterface, labeled [source, default]. The outgoing interface in question must be derived from <b>IDispatch</b>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo2">IProvideClassInfo2</a>
