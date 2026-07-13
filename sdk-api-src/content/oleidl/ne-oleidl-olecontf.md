---
UID: NE:oleidl.tagOLECONTF
title: OLECONTF (oleidl.h)
description: Indicates the type of objects to be enumerated.
helpviewer_keywords: ["OLECONTF","OLECONTF enumeration [COM]","OLECONTF_EMBEDDINGS","OLECONTF_LINKS","OLECONTF_ONLYIFRUNNING","OLECONTF_ONLYUSER","OLECONTF_OTHERS","_ole_OLECONTF","com.olecontf","oleidl/OLECONTF","oleidl/OLECONTF_EMBEDDINGS","oleidl/OLECONTF_LINKS","oleidl/OLECONTF_ONLYIFRUNNING","oleidl/OLECONTF_ONLYUSER","oleidl/OLECONTF_OTHERS"]
old-location: com\olecontf.htm
tech.root: com
ms.assetid: 9c70fc86-7166-47dd-a424-741f18e381e3
ms.date: 12/05/2018
ms.keywords: OLECONTF, OLECONTF enumeration [COM], OLECONTF_EMBEDDINGS, OLECONTF_LINKS, OLECONTF_ONLYIFRUNNING, OLECONTF_ONLYUSER, OLECONTF_OTHERS, _ole_OLECONTF, com.olecontf, oleidl/OLECONTF, oleidl/OLECONTF_EMBEDDINGS, oleidl/OLECONTF_LINKS, oleidl/OLECONTF_ONLYIFRUNNING, oleidl/OLECONTF_ONLYUSER, oleidl/OLECONTF_OTHERS
req.header: oleidl.h
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
req.typenames: OLECONTF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLECONTF
 - oleidl/tagOLECONTF
 - OLECONTF
 - oleidl/OLECONTF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLECONTF
---

# OLECONTF enumeration


## -description

Indicates the type of objects 
    to be enumerated.

## -enum-fields

### -field OLECONTF_EMBEDDINGS:1

Enumerates the embedded objects in the container.

### -field OLECONTF_LINKS:2

Enumerates the linked objects in the container.

### -field OLECONTF_OTHERS:4

Enumerates all objects in the container that are not OLE compound document objects (i.e., objects other than 
       linked or embedded objects). Use this flag to enumerate the container's pseudo-objects.

### -field OLECONTF_ONLYUSER:8

Enumerates only those objects the user is aware of. For example, hidden named-ranges in Microsoft Excel would 
       not be enumerated using this value.

### -field OLECONTF_ONLYIFRUNNING:16

Enumerates only those linked or embedded objects that are currently in the running state for this 
       container.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-enumobjects">IOleContainer::EnumObjects</a>



<a href="/windows/desktop/api/vbinterf/nf-vbinterf-ivbgetcontrol-enumcontrols">IVBGetControl::EnumControls</a>
