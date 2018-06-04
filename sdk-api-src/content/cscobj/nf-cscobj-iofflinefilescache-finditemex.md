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

# IOfflineFilesCache::FindItemEx


## -description


Locates a particular file or directory item in the cache.


## -parameters




### -param pszPath [in]

UNC path of the file or directory to be located.


### -param pIncludeFileFilter [in]

If provided, references the filter applied to the decision to include files.  This parameter is optional and can be <b>NULL</b>.


### -param pIncludeDirFilter [in]

If provided, references the filter applied to the decision to include directories.  This parameter is optional and can be <b>NULL</b>.


### -param pExcludeFileFilter [in]

If provided, references the filter applied to the decision to exclude files.  This parameter is optional and can be <b>NULL</b>.


### -param pExcludeDirFilter [in]

If provided, references the "filter" applied to the decision to exclude directories.  This parameter is optional and may be <b>NULL</b>.


### -param dwQueryFlags [in]

Flags affecting the amount of query activity at the time the item is located in the cache. The parameter can contain one or more of the following bit flags.



#### OFFLINEFILES_ITEM_QUERY_REMOTEINFO (0x00000001)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE (0x00000002)

If this flag is set, the find operation includes an extra call to the Offline Files store to obtain information about the connection state (online or offline) of the item.  If this flag is not set, the operation does not include this extra operation, and connection state will be queried on demand when it is requested.

<div class="alert"><b>Note</b>  If you know that you will need connection state for the item, setting this flag is slightly more efficient.  If connection state is not required, it is more efficient to not set this flag.</div>
<div> </div>


#### OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT (0x00000004)

If this flag is set, the find operation includes an extra call to the Offline Files store to obtain information about the amount, in bytes, of unsynchronized ("dirty") data for the associated file in the local Offline Files cache.



#### OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT (0x00000008)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE (0x00000010)

If this flag is set, the find operation includes transparently cached items.



#### OFFLINEFILES_ITEM_QUERY_ADMIN (0x80000000)

Allows administrators to find items cached by any user.  If this flag is set and the caller is not an administrator, the method call fails.


### -param ppItem [out]

Pointer to the <a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a> interface of the cache item.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the cache entry is not found.




## -remarks



<b>FindItemEx</b> is an enhanced version of <a href="https://msdn.microsoft.com/15696dbf-09a9-42e3-8400-20f7b9b171b7">FindItem</a> that provides filtering capabilities similar to what is offered by cache item enumeration.  Calling <b>FindItem</b> is equivalent to calling <b>FindItemEx</b> with all four filter parameters set to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

