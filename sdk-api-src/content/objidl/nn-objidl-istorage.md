---
UID: NN:objidl.IStorage
title: IStorage
author: windows-sdk-content
description: The IStorage interface supports the creation and management of structured storage objects.
old-location: stg\istorage.htm
old-project: stg
ms.assetid: 2f454538-0f40-4811-b908-cd317ef79487
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IStorage, IStorage interface [Structured Storage], IStorage interface [Structured Storage],described, _stg_istorage, objidl/IStorage, stg.istorage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IStorage interface


## -description


The 
<b>IStorage</b> interface supports the creation and management of structured storage objects. Structured storage allows hierarchical storage of information within a single file, and is often referred to as "a file system within a file". Elements of a structured storage object are storages and streams. Storages are analogous to directories, and streams are analogous to files. Within a structured storage there will be a primary storage object that may contain substorages, possibly nested, and streams. Storages provide the structure of the object, and streams contain the data, which is manipulated through the 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface.

The 
<b>IStorage</b> interface provides methods for creating and managing the root storage object, child storage objects, and stream objects. These methods can create, open, enumerate, move, copy, rename, or delete the elements in the storage object.

An application must release its 
<b>IStorage</b> pointers when it is done with the storage object to deallocate memory used. There are also methods for changing the date and time of an element.

There are a number of different modes in which a storage object and its elements can be opened, determined by setting values from <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>. One aspect of this is how changes are committed. You can set direct mode, in which changes to an object are immediately written to it, or transacted mode, in which changes are written to a buffer until explicitly committed. The 
<b>IStorage</b> interface provides methods for committing changes and reverting to the last-committed version. For example, a stream can be opened in read-only mode or read/write mode. For more information, see <b>STGM Constants</b>.

Other methods provide access to information about a storage object and its elements through the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Reflects changes for a transacted storage object to the parent level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b25b32b-f739-406a-96e8-dba687c7f055">CopyTo</a>
</td>
<td align="left" width="63%">
Copies the entire contents of this open storage object into another storage object. The layout of the destination storage object may differ.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c74cacf-8d3c-4d57-b1e9-dc5e4f281717">CreateStorage</a>
</td>
<td align="left" width="63%">
Creates and opens a new storage object within this storage object. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/168f5ac9-8a72-4356-82a4-de3a7ec72c05">CreateStream</a>
</td>
<td align="left" width="63%">
Creates and opens a stream object with the specified name contained in this storage object. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70ad7f8c-15ea-42f1-ac18-006bc6ad5e81">DestroyElement</a>
</td>
<td align="left" width="63%">
Removes the specified storage or stream from this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29ca157e-40e2-4e9a-95fb-a31bb45570f2">EnumElements</a>
</td>
<td align="left" width="63%">
Returns an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9d33c64-edac-480f-b295-b2a06e51af2e">MoveElementTo</a>
</td>
<td align="left" width="63%">
Copies or moves a substorage or stream from this storage object to another storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1f0564e-0ecd-4b73-8863-9d6b6746fd02">OpenStorage</a>
</td>
<td align="left" width="63%">
Opens an existing storage object with the specified name according to the specified access mode. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb">OpenStream</a>
</td>
<td align="left" width="63%">
Opens an existing stream object within this storage object using the specified access permissions in <i>grfMode</i>. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d88b2e0-8b68-4607-8f96-5e36e831c283">RenameElement</a>
</td>
<td align="left" width="63%">
Renames the specified storage or stream in this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b7626e-bad1-47b5-8bcd-3da3b05c53c4">Revert</a>
</td>
<td align="left" width="63%">
Discards all changes that have been made to the storage object since the last commit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02ab2708-fc8b-4941-939a-a819cf823108">SetClass</a>
</td>
<td align="left" width="63%">
Assigns the specified CLSID to this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6a1fba4-0444-4de3-a838-2d339878fe24">SetElementTimes</a>
</td>
<td align="left" width="63%">
Sets the modification, access, and creation times of the indicated storage element, if supported by the underlying file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52606df8-10ea-40e7-bb61-c86c7b7262d2">SetStateBits</a>
</td>
<td align="left" width="63%">
Stores up to 32 bits of state information in this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">Stat</a>
</td>
<td align="left" width="63%">
Returns the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure for this open storage object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>
 

 

