---
UID: NF:cscobj.IOfflineFilesItemContainer.EnumItemsEx
title: IOfflineFilesItemContainer::EnumItemsEx (cscobj.h)
description: Returns an enumerator of child items for the cache item implementing this method. (IOfflineFilesItemContainer.EnumItemsEx)
helpviewer_keywords: ["EnumItemsEx","EnumItemsEx method [Offline Files]","EnumItemsEx method [Offline Files]","IOfflineFilesItemContainer interface","IOfflineFilesItemContainer interface [Offline Files]","EnumItemsEx method","IOfflineFilesItemContainer.EnumItemsEx","IOfflineFilesItemContainer::EnumItemsEx","OFFLINEFILES_ENUM_FLAT","OFFLINEFILES_ENUM_FLAT_FILESONLY","OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE","OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE","OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT","OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT","OFFLINEFILES_ITEM_QUERY_REMOTEINFO","cscobj/IOfflineFilesItemContainer::EnumItemsEx","of.iofflinefilesitemcontainer_enumitemsex"]
old-location: of\iofflinefilesitemcontainer_enumitemsex.htm
tech.root: of
ms.assetid: 001d384f-013d-41c0-a636-40206a33508d
ms.date: 12/05/2018
ms.keywords: EnumItemsEx, EnumItemsEx method [Offline Files], EnumItemsEx method [Offline Files],IOfflineFilesItemContainer interface, IOfflineFilesItemContainer interface [Offline Files],EnumItemsEx method, IOfflineFilesItemContainer.EnumItemsEx, IOfflineFilesItemContainer::EnumItemsEx, OFFLINEFILES_ENUM_FLAT, OFFLINEFILES_ENUM_FLAT_FILESONLY, OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE, OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE, OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEINFO, cscobj/IOfflineFilesItemContainer::EnumItemsEx, of.iofflinefilesitemcontainer_enumitemsex
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesItemContainer::EnumItemsEx
 - cscobj/IOfflineFilesItemContainer::EnumItemsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesItemContainer.EnumItemsEx
---

# IOfflineFilesItemContainer::EnumItemsEx


## -description

Returns an enumerator of child items for the cache item implementing this method. Server, share, and directory entries in the Offline Files cache implement this method to expose the enumeration of their immediate children.  However, a call to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to query a file item for <b>IID_IOfflineFilesItemContainer</b> fails with <b>E_NOINTERFACE</b>, because file items have no children.

This method is similar to <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemcontainer-enumitems">IOfflineFilesItemContainer::EnumItems</a>, except that it allows filtering and flat enumeration.

## -parameters

### -param pIncludeFileFilter [in]

If provided, references the filter applied to the decision to include files.  This parameter is optional and can be <b>NULL</b>.

### -param pIncludeDirFilter [in]

If provided, references the filter applied to the decision to include directories.  This parameter is optional and can be <b>NULL</b>.

### -param pExcludeFileFilter [in]

If provided, references the filter applied to the decision to exclude files.  This parameter is optional and can be <b>NULL</b>.

### -param pExcludeDirFilter [in]

If provided, references the filter applied to the decision to exclude directories.  This parameter is optional and can be <b>NULL</b>.

### -param dwEnumFlags [in]

Flags affecting the type of enumeration performed.  The parameter may contain one or more of the following flag bits.



#### OFFLINEFILES_ENUM_FLAT (0x00000001)

If this flag is set, the returned enumerator will enumerate all of the item's descendants in the offline files cache.  If this flag is not set, only the item's immediate children are enumerated.



#### OFFLINEFILES_ENUM_FLAT_FILESONLY (0x00000002)

If this flag is set, only file items are returned in the enumeration.  Server, share, and directory entries are not included.  This flag has no effect if the <b>OFFLINEFILES_ENUM_FLAT</b> flag is not set.

### -param dwQueryFlags [in]

Flags affecting the amount of query activity at the time of enumeration.  The parameter can contain one or more of the following bit flags.



#### OFFLINEFILES_ITEM_QUERY_REMOTEINFO (0x00000001)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE (0x00000002)

If this flag is set, the enumeration operation includes an extra call to the Offline Files store to obtain information about the connection state (online or offline) of the item.  If this flag is not set, enumeration does not include this extra operation.



#### OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT (0x00000004)

If this flag is set, the find operation includes an extra call to the Offline Files store to obtain information about the amount, in bytes, of unsynchronized ("dirty") data for the associated file in the local Offline Files cache.



#### OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT (0x00000008)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE (0x00000010)

Allows administrators to find items cached by any user. If this flag is set and the caller is not an administrator, the method call fails.

### -param ppenum [out]

Enumerator of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a> interface pointers.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

To begin a top-down enumeration of the entire cache, perform the following steps:

<ol>
<li>Create an instance of <b>CLSID_OfflineFilesCache</b> and obtain its 
      <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a> interface.</li>
<li>Call the <b>EnumItemsEx</b> method to obtain an enumerator for the server entries.</li>
<li>For each entry returned, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for  <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a>.</li>
<li>If <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> succeeds, the item supports children.  If so, enumerate each child, calling <b>QueryInterface</b> for <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a> on each.  This pattern may be recursively applied to enumerate the entire cache.</li>
</ol>
It is possible to provide both inclusion and exclusion filters to the same enumeration. In such a case, the results are as follows for any particular item being evaluated.

<table>
<tr>
<th></th>
<th>Inclusion Match</th>
<th>Inclusion No Match</th>
</tr>
<tr>
<th>Exclusion Match</th>
<td>Excluded</td>
<td>Excluded</td>
</tr>
<tr>
<th>Exclusion No Match</th>
<td>Included</td>
<td>Excluded</td>
</tr>
</table>
 

As the table illustrates, if the exclusion filter matches or the inclusion filter does not match, the item is excluded from enumeration.  For an item to be included in the enumeration, the exclusion filter must not match and the inclusion filter must match.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemcontainer-enumitems">IOfflineFilesItemContainer::EnumItems</a>
