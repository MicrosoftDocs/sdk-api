---
UID: NN:objidl.IStorage
title: IStorage (objidl.h)
author: windows-sdk-content
description: The IStorage interface supports the creation and management of structured storage objects.
old-location: stg\istorage.htm
tech.root: Stg
ms.assetid: 2f454538-0f40-4811-b908-cd317ef79487
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStorage, IStorage interface [Structured Storage], IStorage interface [Structured Storage],described, _stg_istorage, objidl/IStorage, stg.istorage
ms.topic: interface
f1_keywords: 
 - "objidl/IStorage"
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
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorage interface


## -description


The 
<b>IStorage</b> interface supports the creation and management of structured storage objects. Structured storage allows hierarchical storage of information within a single file, and is often referred to as "a file system within a file". Elements of a structured storage object are storages and streams. Storages are analogous to directories, and streams are analogous to files. Within a structured storage there will be a primary storage object that may contain substorages, possibly nested, and streams. Storages provide the structure of the object, and streams contain the data, which is manipulated through the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface.

The 
<b>IStorage</b> interface provides methods for creating and managing the root storage object, child storage objects, and stream objects. These methods can create, open, enumerate, move, copy, rename, or delete the elements in the storage object.

An application must release its 
<b>IStorage</b> pointers when it is done with the storage object to deallocate memory used. There are also methods for changing the date and time of an element.

There are a number of different modes in which a storage object and its elements can be opened, determined by setting values from <a href="https://docs.microsoft.com/windows/desktop/Stg/stgm-constants">STGM Constants</a>. One aspect of this is how changes are committed. You can set direct mode, in which changes to an object are immediately written to it, or transacted mode, in which changes are written to a buffer until explicitly committed. The 
<b>IStorage</b> interface provides methods for committing changes and reverting to the last-committed version. For example, a stream can be opened in read-only mode or read/write mode. For more information, see <b>STGM Constants</b>.

Other methods provide access to information about a storage object and its elements through the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStorage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStorage</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-commit">Commit</a>
</td>
<td align="left" width="63%">
Reflects changes for a transacted storage object to the parent level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-copyto">CopyTo</a>
</td>
<td align="left" width="63%">
Copies the entire contents of this open storage object into another storage object. The layout of the destination storage object may differ.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-createstorage">CreateStorage</a>
</td>
<td align="left" width="63%">
Creates and opens a new storage object within this storage object. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-createstream">CreateStream</a>
</td>
<td align="left" width="63%">
Creates and opens a stream object with the specified name contained in this storage object. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-destroyelement">DestroyElement</a>
</td>
<td align="left" width="63%">
Removes the specified storage or stream from this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-enumelements">EnumElements</a>
</td>
<td align="left" width="63%">
Returns an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-moveelementto">MoveElementTo</a>
</td>
<td align="left" width="63%">
Copies or moves a substorage or stream from this storage object to another storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-openstorage">OpenStorage</a>
</td>
<td align="left" width="63%">
Opens an existing storage object with the specified name according to the specified access mode. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-openstream">OpenStream</a>
</td>
<td align="left" width="63%">
Opens an existing stream object within this storage object using the specified access permissions in <i>grfMode</i>. The name must not exceed 31 characters in length (not including the string terminator). The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-renameelement">RenameElement</a>
</td>
<td align="left" width="63%">
Renames the specified storage or stream in this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-revert">Revert</a>
</td>
<td align="left" width="63%">
Discards all changes that have been made to the storage object since the last commit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-setclass">SetClass</a>
</td>
<td align="left" width="63%">
Assigns the specified CLSID to this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-setelementtimes">SetElementTimes</a>
</td>
<td align="left" width="63%">
Sets the modification, access, and creation times of the indicated storage element, if supported by the underlying file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-setstatebits">SetStateBits</a>
</td>
<td align="left" width="63%">
Stores up to 32 bits of state information in this storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">Stat</a>
</td>
<td align="left" width="63%">
Returns the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure for this open storage object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/samples">Samples</a>
 

 

