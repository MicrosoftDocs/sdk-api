---
UID: NE:oleidl.tagOLEVERBATTRIB
title: OLEVERBATTRIB (oleidl.h)
description: Describes the attributes of a specified verb for an object.
helpviewer_keywords: ["OLEVERBATTRIB","OLEVERBATTRIB enumeration [COM]","OLEVERBATTRIB_NEVERDIRTIES","OLEVERBATTRIB_ONCONTAINERMENU","_ole_OLEVERBATTRIB","com.oleverbattrib","oleidl/OLEVERBATTRIB","oleidl/OLEVERBATTRIB_NEVERDIRTIES","oleidl/OLEVERBATTRIB_ONCONTAINERMENU"]
old-location: com\oleverbattrib.htm
tech.root: com
ms.assetid: 797498ba-5ad6-4476-87d8-de85b30396f4
ms.date: 12/05/2018
ms.keywords: OLEVERBATTRIB, OLEVERBATTRIB enumeration [COM], OLEVERBATTRIB_NEVERDIRTIES, OLEVERBATTRIB_ONCONTAINERMENU, _ole_OLEVERBATTRIB, com.oleverbattrib, oleidl/OLEVERBATTRIB, oleidl/OLEVERBATTRIB_NEVERDIRTIES, oleidl/OLEVERBATTRIB_ONCONTAINERMENU
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
req.typenames: OLEVERBATTRIB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEVERBATTRIB
 - oleidl/tagOLEVERBATTRIB
 - OLEVERBATTRIB
 - oleidl/OLEVERBATTRIB
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
 - OLEVERBATTRIB
---

# OLEVERBATTRIB enumeration


## -description

Describes the attributes of a specified verb for an object.

## -enum-fields

### -field OLEVERBATTRIB_NEVERDIRTIES:1

Executing this verb will not cause the object to become dirty and is therefore in need of saving to persistent storage.

### -field OLEVERBATTRIB_ONCONTAINERMENU:2

Indicates a verb that should appear in the container's menu of verbs for this object. OLEIVERB_HIDE, OLEIVERB_SHOW, and OLEIVERB_OPEN never have this value set.

## -remarks

Values are used in the enumerator (which supports the <a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a> interface) that is created by a call to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>



<a href="/windows/desktop/api/oleidl/ns-oleidl-oleverb">OLEVERB</a>
