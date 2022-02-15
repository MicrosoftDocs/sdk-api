---
UID: NE:wmp.WMPStringCollectionChangeEventType
title: WMPStringCollectionChangeEventType (wmp.h)
description: The WMPStringCollectionChangeEventType enumeration type defines the types of changes that can occur in a string collection.
helpviewer_keywords: ["WMPStringCollectionChangeEventType","WMPStringCollectionChangeEventType enumeration [Windows Media Player]","wmp.wmpstringcollectionchangeeventtype","wmp/WMPStringCollectionChangeEventType","wmp/wmpsccetBeginUpdates","wmp/wmpsccetChange","wmp/wmpsccetClear","wmp/wmpsccetDelete","wmp/wmpsccetEndUpdates","wmp/wmpsccetInsert","wmp/wmpsccetUnknown","wmpsccetBeginUpdates","wmpsccetChange","wmpsccetClear","wmpsccetDelete","wmpsccetEndUpdates","wmpsccetInsert","wmpsccetUnknown"]
old-location: wmp\wmpstringcollectionchangeeventtype.htm
tech.root: WMP
ms.assetid: 7690972b-52ac-4249-baa5-3d2b38a4487a
ms.date: 12/05/2018
ms.keywords: WMPStringCollectionChangeEventType, WMPStringCollectionChangeEventType enumeration [Windows Media Player], wmp.wmpstringcollectionchangeeventtype, wmp/WMPStringCollectionChangeEventType, wmp/wmpsccetBeginUpdates, wmp/wmpsccetChange, wmp/wmpsccetClear, wmp/wmpsccetDelete, wmp/wmpsccetEndUpdates, wmp/wmpsccetInsert, wmp/wmpsccetUnknown, wmpsccetBeginUpdates, wmpsccetChange, wmpsccetClear, wmpsccetDelete, wmpsccetEndUpdates, wmpsccetInsert, wmpsccetUnknown
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
req.target-min-winversvr: 
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
req.typenames: WMPStringCollectionChangeEventType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPStringCollectionChangeEventType
 - wmp/WMPStringCollectionChangeEventType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPStringCollectionChangeEventType
---

# WMPStringCollectionChangeEventType enumeration


## -description

The <b>WMPStringCollectionChangeEventType</b> enumeration type defines the types of changes that can occur in a string collection.



<b>Syntax</b>

## -enum-fields

### -field wmpsccetUnknown:0

Not a valid event type.

### -field wmpsccetInsert

An item was inserted.

### -field wmpsccetChange

The string collection changed.

### -field wmpsccetDelete

An item was deleted.

### -field wmpsccetClear

The string collection was cleared.

### -field wmpsccetBeginUpdates

Bulk updates are beginning.

### -field wmpsccetEndUpdates

Bulk updates have ended.

## -remarks

Windows Media Player 10 Mobile: This enumeration is not supported.

## -see-also

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange">IWMPEvents3::StringCollectionChange</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection">IWMPStringCollection Interface</a>



<a href="/windows/desktop/WMP/interfaces">Interfaces</a>
