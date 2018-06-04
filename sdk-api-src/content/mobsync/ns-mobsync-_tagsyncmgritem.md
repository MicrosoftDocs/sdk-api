---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# _tagSYNCMGRITEM structure


## -description


Provides information about items being enumerated by the <a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a> interface.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure.


### -field dwFlags

Type: <b>DWORD</b>

One or more values from the <a href="https://msdn.microsoft.com/6297f10b-9a2c-4077-9dca-e5c0850d125a">SYNCMGRITEMFLAGS</a> enumeration.


### -field ItemID

Type: <b>GUID</b>

The identifier for this item.


### -field dwItemState

Type: <b>DWORD</b>

Indicates whether this item is included in synchronization operations. This member can have one of the following values.



#### SYNCMGRITEMSTATE_UNCHECKED (0)

The default is not including this item in synchronization operations.



#### SYNCMGRITEMSTATE_CHECKED (1)

The default is including this item in synchronization operations.


### -field hIcon

Type: <b>HICON</b>

The icon for this item.


### -field wszItemName

Type: <b>WCHAR[MAX_SYNCMGRITEMNAME]</b>

The name of this item.


### -field ftLastUpdate

Type: <b>FILETIME</b>

The time of the last synchronization for this item.


## -see-also




<a href="https://msdn.microsoft.com/6297f10b-9a2c-4077-9dca-e5c0850d125a">SYNCMGRITEMFLAGS</a>
 

 

