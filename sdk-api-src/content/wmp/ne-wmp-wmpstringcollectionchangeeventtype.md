---
UID: NE:wmp.WMPStringCollectionChangeEventType
title: WMPStringCollectionChangeEventType (wmp.h)
author: windows-sdk-content
description: The WMPStringCollectionChangeEventType enumeration type defines the types of changes that can occur in a string collection.
old-location: wmp\wmpstringcollectionchangeeventtype.htm
tech.root: WMP
ms.assetid: 7690972b-52ac-4249-baa5-3d2b38a4487a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMPStringCollectionChangeEventType, WMPStringCollectionChangeEventType enumeration [Windows Media Player], wmp.wmpstringcollectionchangeeventtype, wmp/WMPStringCollectionChangeEventType, wmp/wmpsccetBeginUpdates, wmp/wmpsccetChange, wmp/wmpsccetClear, wmp/wmpsccetDelete, wmp/wmpsccetEndUpdates, wmp/wmpsccetInsert, wmp/wmpsccetUnknown, wmpsccetBeginUpdates, wmpsccetChange, wmpsccetClear, wmpsccetDelete, wmpsccetEndUpdates, wmpsccetInsert, wmpsccetUnknown
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPStringCollectionChangeEventType
product: Windows
targetos: Windows
req.typenames: WMPStringCollectionChangeEventType
req.redist: 
ms.custom: 19H1
---

# WMPStringCollectionChangeEventType enumeration


## -description



The <b>WMPStringCollectionChangeEventType</b> enumeration type defines the types of changes that can occur in a string collection.



<b>Syntax</b>


## -enum-fields




### -field wmpsccetUnknown

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




<a href="https://msdn.microsoft.com/90689fb7-656d-4c06-a0a9-02bbe0e5b5dd">Enumeration Types</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563307(v=VS.85).aspx">IWMPEvents3::StringCollectionChange</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563686(v=VS.85).aspx">IWMPStringCollection Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

