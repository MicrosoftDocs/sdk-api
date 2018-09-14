---
UID: NF:cscobj.IOfflineFilesCache.DeleteItems
title: IOfflineFilesCache::DeleteItems
author: windows-sdk-content
description: Deletes files and directories from the local cache.
old-location: of\iofflinefilescache_deleteitems.htm
tech.root: OfflineFiles
ms.assetid: e6326364-fbd0-4446-97c3-6a3940856efb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DeleteItems, DeleteItems method [Offline Files], DeleteItems method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],DeleteItems method, IOfflineFilesCache.DeleteItems, IOfflineFilesCache::DeleteItems, OFFLINEFILES_DELETE_FLAG_ADMIN, OFFLINEFILES_DELETE_FLAG_DELMODIFIED, OFFLINEFILES_DELETE_FLAG_NOAUTOCACHED, OFFLINEFILES_DELETE_FLAG_NOPINNED, cscobj/IOfflineFilesCache::DeleteItems, of.iofflinefilescache_deleteitems
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesCache.DeleteItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
Returns HRESULT_FROM_WIN32(ERROR_MORE_DATA)  if errors occurred during the operation.  Use the <a href="https://msdn.microsoft.com/en-us/library/Bb530618(v=VS.85).aspx">IOfflineFilesSimpleProgress::ItemResult</a> callback method to detect errors as they occur.




## -remarks



The caller must have sufficient access to the files and directories to be deleted.

If a delete operation is canceled while in progress, changes to files processed to that point are not rolled back.

If a delete operation on a directory cannot remove all of its contained files or directories (for example, if access is denied), the specified directory entry is not removed.  Any files and directories deleted up to that point remain deleted.

Files are deleted only from the local cache.  Associated files on the network server are not affected.

Files deleted are not recoverable through the Recycle Bin.  Files deleted must be re-cached to be available offline.

If only one path is provided in the <i>rgpszPaths</i> parameter and that path is to a single file, the return value indicates the result of that single delete operation.  Otherwise, the caller must implement the progress callback methods in the following list and monitor the <a href="https://msdn.microsoft.com/en-us/library/Bb530618(v=VS.85).aspx">IOfflineFilesSimpleProgress::ItemResult</a> method to obtain the result for each processed file and directory.

<table>
<tr>
<th>Progress Events Interface</th>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530596(v=VS.85).aspx">IOfflineFilesProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530597(v=VS.85).aspx">Begin</a>
</td>
<td>Called at the start of the operation.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530616(v=VS.85).aspx">IOfflineFilesSimpleProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530617(v=VS.85).aspx">ItemBegin</a>
</td>
<td>Called at the start of processing for each file.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530616(v=VS.85).aspx">IOfflineFilesSimpleProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530618(v=VS.85).aspx">ItemResult</a>
</td>
<td>Called after each file is deleted.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530596(v=VS.85).aspx">IOfflineFilesProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530599(v=VS.85).aspx">QueryAbort</a>
</td>
<td>Called periodically during the sync operation to detect a request for cancellation.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530596(v=VS.85).aspx">IOfflineFilesProgress</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb530598(v=VS.85).aspx">End</a>
</td>
<td>Called at the end of the operation.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530486(v=VS.85).aspx">IOfflineFilesCache</a>
 

 

