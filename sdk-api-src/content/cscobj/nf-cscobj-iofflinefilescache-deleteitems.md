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

# IOfflineFilesCache::DeleteItems


## -description



    Deletes files and directories from the local cache.  Deleting a container item implies deletion of all its contained items, recursively.


## -parameters




### -param rgpszPaths [in]

Array of pointers, each to a fully qualified UNC path of a file or directory to be deleted.


### -param cPaths [in]

Number of paths in the <i>rgpszPaths</i> array.


### -param dwFlags [in]

Flags controlling the behavior of the delete operation.  This parameter can be one or more of the following values.



#### OFFLINEFILES_DELETE_FLAG_NOAUTOCACHED (0x00000001)

Do not delete automatically cached items.  The default behavior is to delete automatically cached items.



#### OFFLINEFILES_DELETE_FLAG_NOPINNED (0x00000002)

Do not delete pinned items.  The default behavior is to delete pinned items.



#### OFFLINEFILES_DELETE_FLAG_DELMODIFIED (0x00000004)

Delete even if locally modified in the cache.  The default behavior is to not delete files with unsynchronized local changes.



#### OFFLINEFILES_DELETE_FLAG_ADMIN (0x80000000)

Allows administrators to enumerate and delete all files regardless of access rights.  If this flag is set and the caller is not an administrator, the function fails.


### -param bAsync [in]

Indicates if the operation is to be performed asynchronously.  If this parameter is <b>TRUE</b>, the operation is scheduled for asynchronous operation and the function returns immediately.  If this parameter is <b>FALSE</b>, the function returns when the operation is complete.


### -param pIProgress [in]

Interface to an event sink that will receive progress events during the operation.  If events are not desired, this parameter may be <b>NULL</b>.  Providing an event sink is highly recommended for asynchronous operation.  A progress implementation is the only way to be notified when the asynchronous operation completes.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_CANCELLED)</code>  if the operation is canceled.
Returns HRESULT_FROM_WIN32(ERROR_MORE_DATA)  if errors occurred during the operation.  Use the <a href="https://msdn.microsoft.com/60ed3b12-b56e-4a58-8e37-a4a745ddb783">IOfflineFilesSimpleProgress::ItemResult</a> callback method to detect errors as they occur.




## -remarks



The caller must have sufficient access to the files and directories to be deleted.

If a delete operation is canceled while in progress, changes to files processed to that point are not rolled back.

If a delete operation on a directory cannot remove all of its contained files or directories (for example, if access is denied), the specified directory entry is not removed.  Any files and directories deleted up to that point remain deleted.

Files are deleted only from the local cache.  Associated files on the network server are not affected.

Files deleted are not recoverable through the Recycle Bin.  Files deleted must be re-cached to be available offline.

If only one path is provided in the <i>rgpszPaths</i> parameter and that path is to a single file, the return value indicates the result of that single delete operation.  Otherwise, the caller must implement the progress callback methods in the following list and monitor the <a href="https://msdn.microsoft.com/60ed3b12-b56e-4a58-8e37-a4a745ddb783">IOfflineFilesSimpleProgress::ItemResult</a> method to obtain the result for each processed file and directory.

<table>
<tr>
<th>Progress Events Interface</th>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/d3fe6abf-fc0c-4bba-9c9f-5d0e77c27b43">Begin</a>
</td>
<td>Called at the start of the operation.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/490f0958-125b-4c09-8ca4-07532ed8d4d4">IOfflineFilesSimpleProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/0e3496ee-e987-4c37-93ff-bc8409acabde">ItemBegin</a>
</td>
<td>Called at the start of processing for each file.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/490f0958-125b-4c09-8ca4-07532ed8d4d4">IOfflineFilesSimpleProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/60ed3b12-b56e-4a58-8e37-a4a745ddb783">ItemResult</a>
</td>
<td>Called after each file is deleted.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/24b95898-0fe6-420b-83f2-ac77f493aeab">QueryAbort</a>
</td>
<td>Called periodically during the sync operation to detect a request for cancellation.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/b3d09f2e-29d5-496f-a046-4ba067e642a6">End</a>
</td>
<td>Called at the end of the operation.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

