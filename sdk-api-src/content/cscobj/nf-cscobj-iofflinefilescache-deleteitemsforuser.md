---
UID: NF:cscobj.IOfflineFilesCache.DeleteItemsForUser
title: IOfflineFilesCache::DeleteItemsForUser
author: windows-sdk-content
description: Deletes a user's files and directories from the local cache.
old-location: of\iofflinefilescache_deleteitemsforuser.htm
old-project: OfflineFiles
ms.assetid: a187fd6b-0717-4663-b460-df96876cd9c3
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DeleteItemsForUser, DeleteItemsForUser method [Offline Files], DeleteItemsForUser method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],DeleteItemsForUser method, IOfflineFilesCache.DeleteItemsForUser, IOfflineFilesCache::DeleteItemsForUser, OFFLINEFILES_DELETE_FLAG_ADMIN, OFFLINEFILES_DELETE_FLAG_DELMODIFIED, OFFLINEFILES_DELETE_FLAG_NOAUTOCACHED, OFFLINEFILES_DELETE_FLAG_NOPINNED, cscobj/IOfflineFilesCache::DeleteItemsForUser, of.iofflinefilescache_deleteitemsforuser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesCache.DeleteItemsForUser
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesCache::DeleteItemsForUser


## -description



    Deletes a user's files and directories from the local cache.  Deleting a container item implies deletion of all its contained items, recursively.


## -parameters




### -param pszUser [in]

Text string identifying the user for which the files are to be deleted for.  This option is available only to administrators on the local computer.  The text string may be the user's SID in string format or the user's <i>domain\user</i> logon name string.


### -param rgpszPaths [in]

Array of pointers, each to a fully qualified UNC path of a file or directory to be deleted.


### -param cPaths [in]

Number of paths in <i>rgpszPaths</i>.


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

Indicates whether the operation is to be performed asynchronously.  If this parameter is <b>TRUE</b>, the operation is scheduled for asynchronous operation and the function returns immediately.  If this parameter is <b>FALSE</b>, the function returns when the operation is complete.


### -param pIProgress [in]

Interface to an event sink that will receive progress events during the operation.  If events are not desired, this parameter can be <b>NULL</b>.  Providing an event sink is highly recommended for asynchronous operation.  A progress implementation is the only way to be notified when the asynchronous operation completes.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_CANCELLED)</code>  if the operation is canceled.
Returns <code>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</code>  if errors occurred during the operation.  Use the <a href="https://msdn.microsoft.com/60ed3b12-b56e-4a58-8e37-a4a745ddb783">IOfflineFilesSimpleProgress::ItemResult</a> callback method to detect errors as they occur.




## -remarks



The caller must have sufficient access to the files and directories to be deleted.

If a delete operation is canceled while in progress, changes to files processed to that point are not rolled back.

If a delete operation on a directory cannot remove all of its contained files or directories (for example, if access is denied), the specified directory entry is not removed.  Any files and directories deleted up to that point remain deleted.

Files are deleted only from the local cache.  Associated files on the network server are not affected.

Files deleted are not recoverable through the Recycle Bin.  Files deleted must be recached to be available offline.

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
<a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/c1cdbc30-bcc9-4023-a3a2-070fb9958609">SyncItemBegin</a>
</td>
<td>Called at the start of processing for each file.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/2a93d52e-6b91-4d91-9372-5f0718621841">SyncItemResult</a>
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
 

 

