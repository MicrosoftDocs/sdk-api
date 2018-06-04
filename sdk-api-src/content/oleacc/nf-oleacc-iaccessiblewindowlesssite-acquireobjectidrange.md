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

# IAccessibleWindowlessSite::AcquireObjectIdRange


## -description


Acquires a range of object IDs from the control host and marks them as reserved by a specific windowless control.  


## -parameters




### -param rangeSize [in]

The size of the object ID range that is being requested.


### -param pRangeOwner




### -param pRangeBase [out]

The first object ID in the acquired range.


#### - pControl [in, optional]

The windowless control that is requesting the range.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To avoid using an object ID that belongs to another windowless control, a control should acquire an object ID range before calling the <a href="https://msdn.microsoft.com/08e74d45-95b6-44c2-a2e0-5ba6ffdcd56a">NotifyWinEvent</a> function.  A control should acquire enough object IDs for all of its contained accessible objects.  For example, a tree control with 100 children would reserve at least 101 object IDs, one for the root, and one for each child.  A tree control that is expected to grow would reserve as many object IDs as expected. If the tree control is expected to grow by several hundred children, it would reserve a range of 1000 IDs just to be safe.  



When the window that contains the Microsoft ActiveX control receives a <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message with an <b>LPARAM</b> value (object ID) that is in a reserved range, it should call the <a href="https://msdn.microsoft.com/c552b26a-a8db-42a1-85c9-9578230def74">IAccessibleHandler::AccessibleObjectFromID</a> method to get an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> object for that object ID.




## -see-also




<a href="https://msdn.microsoft.com/1ED23B39-231B-46A2-9FED-969A36DA8DD9">IAccessibleWindowlessSite</a>



<a href="https://msdn.microsoft.com/CC7AEE46-88BE-445C-A377-C9E8C2B505D3">IAccessibleWindowlessSite::ReleaseObjectIdRange</a>
 

 

