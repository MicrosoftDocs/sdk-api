---
UID: NE:wmp.WMPStringCollectionChangeEventType
title: WMPStringCollectionChangeEventType
author: windows-sdk-content
description: The WMPStringCollectionChangeEventType enumeration type defines the types of changes that can occur in a string collection.
old-location: wmp\wmpstringcollectionchangeeventtype.htm
old-project: WMP
ms.assetid: 7690972b-52ac-4249-baa5-3d2b38a4487a
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: WMPStringCollectionChangeEventType, WMPStringCollectionChangeEventType enumeration [Windows Media Player], wmp.wmpstringcollectionchangeeventtype, wmp/WMPStringCollectionChangeEventType, wmp/wmpsccetBeginUpdates, wmp/wmpsccetChange, wmp/wmpsccetClear, wmp/wmpsccetDelete, wmp/wmpsccetEndUpdates, wmp/wmpsccetInsert, wmp/wmpsccetUnknown, wmpsccetBeginUpdates, wmpsccetChange, wmpsccetClear, wmpsccetDelete, wmpsccetEndUpdates, wmpsccetInsert, wmpsccetUnknown
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPStringCollectionChangeEventType
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/93880116-e354-49d0-ba02-391fbb4d3f8c">IWMPEvents3::StringCollectionChange</a>



<a href="https://msdn.microsoft.com/8cdabea9-7e37-4e63-9d6c-b6f63aa536ea">IWMPStringCollection Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

