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

# IShellFolder2::GetDefaultColumn


## -description


Gets the default sorting and display columns.


## -parameters




### -param dwRes




### -param pSort [out]

Type: <b>ULONG*</b>

A pointer to a value that receives the index of the default sorted column.


### -param pDisplay [out]

Type: <b>ULONG*</b>

A pointer to a value that receives the index of the default display column.


#### - dwReserved [in]

Type: <b>DWORD</b>

Reserved. Set to zero.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



<h3><a id="Notes_to_Users"></a><a id="notes_to_users"></a><a id="NOTES_TO_USERS"></a>Notes to Users</h3>

			Both column indexes returned by this method are intended for use by an application that is presenting a folder view of this folder.

The column specified by 
				<i>pSort</i> is the one that should be used for sorting the items in the folder. To determine the sorting order of any pair of items, pass their PIDLs to <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">CompareIDs</a>. Specify the column by setting the 
				<i>lParam</i> parameter of <b>CompareIDs</b> to the value pointed to by 
				<i>pSort</i>.

If a view will display only one string to represent an item, it should be taken from the column specified by 
				<i>pDisplay</i>. Pass the column index and the item's PIDL to <a href="https://msdn.microsoft.com/bd9e8b6c-ed70-455e-8316-ac0868493802">IShellFolder2::GetDetailsOf</a> to retrieve the string.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method is part of a namespace extension's folder object implementation. It is typically called by a folder view object to ask the folder object which column in Microsoft Windows Explorer Details view should be used to sort the items in the folder. For example, a folder object that represents a transaction log might set 
				<i>pSort</i> to the column that displays the transaction time. The items will then be sorted by the time the transaction took place, rather than by name.

Some clients might call this method to request the index of the column with the names that should be displayed in tree view. Set 
				<i>pDisplay</i> to the appropriate column index. The client will then obtain the display names by calling <a href="https://msdn.microsoft.com/bd9e8b6c-ed70-455e-8316-ac0868493802">IShellFolder2::GetDetailsOf</a>.



