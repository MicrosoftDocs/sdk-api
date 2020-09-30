---
UID: NF:cscobj.IOfflineFilesCache.Unpin
title: IOfflineFilesCache::Unpin (cscobj.h)
description: Unpins files, directories, and network shared folders from the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesCache interface [Offline Files]","Unpin method","IOfflineFilesCache.Unpin","IOfflineFilesCache::Unpin","OFFLINEFILES_PIN_CONTROL_FLAG_ASYNCPROGRESS","OFFLINEFILES_PIN_CONTROL_FLAG_BACKGROUND","OFFLINEFILES_PIN_CONTROL_FLAG_CONSOLE","OFFLINEFILES_PIN_CONTROL_FLAG_FILL","OFFLINEFILES_PIN_CONTROL_FLAG_FORALL","OFFLINEFILES_PIN_CONTROL_FLAG_FORREDIR","OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER","OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER_POLICY","OFFLINEFILES_PIN_CONTROL_FLAG_INTERACTIVE","OFFLINEFILES_PIN_CONTROL_FLAG_LOWPRIORITY","OFFLINEFILES_PIN_CONTROL_PINLINKTARGETS","Unpin","Unpin method [Offline Files]","Unpin method [Offline Files]","IOfflineFilesCache interface","cscobj/IOfflineFilesCache::Unpin","of.iofflinefilescache_unpin"]
old-location: of\iofflinefilescache_unpin.htm
tech.root: of
ms.assetid: 32d81a75-8845-4bd5-a0ff-e056a06ac11c
ms.date: 12/05/2018
ms.keywords: IOfflineFilesCache interface [Offline Files],Unpin method, IOfflineFilesCache.Unpin, IOfflineFilesCache::Unpin, OFFLINEFILES_PIN_CONTROL_FLAG_ASYNCPROGRESS, OFFLINEFILES_PIN_CONTROL_FLAG_BACKGROUND, OFFLINEFILES_PIN_CONTROL_FLAG_CONSOLE, OFFLINEFILES_PIN_CONTROL_FLAG_FILL, OFFLINEFILES_PIN_CONTROL_FLAG_FORALL, OFFLINEFILES_PIN_CONTROL_FLAG_FORREDIR, OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER, OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER_POLICY, OFFLINEFILES_PIN_CONTROL_FLAG_INTERACTIVE, OFFLINEFILES_PIN_CONTROL_FLAG_LOWPRIORITY, OFFLINEFILES_PIN_CONTROL_PINLINKTARGETS, Unpin, Unpin method [Offline Files], Unpin method [Offline Files],IOfflineFilesCache interface, cscobj/IOfflineFilesCache::Unpin, of.iofflinefilescache_unpin
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
 - IOfflineFilesCache::Unpin
 - cscobj/IOfflineFilesCache::Unpin
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
 - IOfflineFilesCache.Unpin
---

# IOfflineFilesCache::Unpin


## -description

Unpins files, directories, and network shared folders from the Offline Files cache. Pinning is called "Always Available Offline" in the Windows user interface.

When a file is unpinned, it is no longer guaranteed to be available offline.  If the unpin operation removes all instances of pin information in that it is not pinned by Folder Redirection, Group Policy, or by the user and that item has no unsynchronized offline changes, it may be automatically removed from the cache at any time.

## -parameters

### -param hwndParent [in]

Identifies the parent window for any user interface elements displayed. This parameter is ignored if the <b>OFFLINEFILES_PIN_CONTROL_FLAG_INTERACTIVE</b> flag is not set in the <i>dwPinControlFlags</i> parameter.

### -param rgpszPaths [in]

Array of pointers, each to a fully qualified UNC path of a file or directory to be unpinned.

### -param cPaths [in]

Number of paths in the <i>rgpszPaths</i> array.

### -param bDeep [in]

If one or more of the paths provided refers to a directory or shared folder, this argument indicates whether all subdirectories are to be unpinned as well.  If this parameter is <b>TRUE</b>, all subdirectories are unpinned recursively.  If this parameter is <b>FALSE</b>, only files that are immediate children of the directory are unpinned.

### -param bAsync [in]

Indicates if the operation is to be performed asynchronously.  If this parameter is <b>TRUE</b>, the operation is scheduled for asynchronous operation and the function returns immediately.  If this parameter is <b>FALSE</b>, the function returns when the operation is complete.

### -param dwPinControlFlags [in]

Controls the behavior of the unpin operation.  May be one or more of the following flags.



#### OFFLINEFILES_PIN_CONTROL_FLAG_FILL (0x00000001)

Ignored when unpinning.



#### OFFLINEFILES_PIN_CONTROL_PINLINKTARGETS (0x00000010)

Ignored when unpinning.



#### OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER (0x00000020)

Unpins the items for the calling user.  This is the flag typically set for a caller of this function.  It is important to note that Offline Files does not support a true per-user notion of pinning.  When an item is pinned for a user, it is pinned for all users of that machine.  However, the ability to access that pinned file depends on the user's access rights to that file computed while online.



#### OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER_POLICY (0x00000040)

Unpins the items for per-user policy.  This differs from the "FORUSER" flag in that this flag cannot be modified by the user through the Offline Files user interface.  Internally, Offline Files sets this flag when items are unpinned by its Group Policy extension.



#### OFFLINEFILES_PIN_CONTROL_FLAG_FORALL (0x00000080)

Unpins the items for all users of the local machine.  While the pinned state applies to all users, the ability to access a pinned file depends on the user's access rights to that file computed while online.



#### OFFLINEFILES_PIN_CONTROL_FLAG_FORREDIR (0x00000100)

Unpins the items for purposes of folder redirection for the calling user.  Windows Folder Redirection sets this flag when unpinning redirected folders.



#### OFFLINEFILES_PIN_CONTROL_FLAG_LOWPRIORITY (0x00000200)

Reserved for future use.



#### OFFLINEFILES_PIN_CONTROL_FLAG_ASYNCPROGRESS (0x00000400)

Progress is reported to the progress interface asynchronously with the actual operations.  For more information about behavior, see the Asynchronous Progress Notifications section.  If this flag is not set, progress is reported synchronously with each operation.



#### OFFLINEFILES_PIN_CONTROL_FLAG_INTERACTIVE (0x00000800)

Set this flag if the operation is allowed to display user interface elements as necessary.  An example is the system's credential-request dialog.  If this flag is set, the value in <i>hwndParent</i> is used as the parent for any user interface elements displayed.



#### OFFLINEFILES_PIN_CONTROL_FLAG_CONSOLE (0x00001000)

This flag is ignored if the "interactive" flag is not set.  If the "interactive" flag is set, this flag indicates that any UI produced should be directed to the console window associated with the process invoking the operation.



#### OFFLINEFILES_PIN_CONTROL_FLAG_BACKGROUND (0x00010000)

Set this flag if you want the unpin operation to avoid sharing violations in the event that an application wishes to open a file that is currently open for the pin operation.  When that scenario occurs and this flag is set, the unpin operation will "back off" and not finish for that particular file at that time.  This flag is primarily used by the Offline Files service for internal operations.

### -param pIProgress [in]

Interface to an event sink that will receive progress events during the operation.  If events are not desired, this parameter may be <b>NULL</b>.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_CANCELLED)</code> if the operation is canceled.

## -remarks

If a unpin operation involving multiple files is canceled while in progress, changes to files processed to that point are not rolled back.

If only one path is provided in the <i>rgpszPaths</i> parameter and that path is to a single file, the return value indicates the result of that single unpin operation.  Otherwise, the caller must implement the progress callback methods in the following list and monitor the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitemresult">IOfflineFilesSyncProgress::SyncItemResult</a> method to obtain the result for each processed file and directory.

<table>
<tr>
<th>Progress Events Interface</th>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-begin">Begin</a>
</td>
<td>Called at the start of the operation.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncprogress">IOfflineFilesSyncProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitembegin">SyncItemBegin</a>
</td>
<td>Called at the start of processing for each file.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncprogress">IOfflineFilesSyncProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitemresult">SyncItemResult</a>
</td>
<td>Called after each file is unpinned.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-queryabort">QueryAbort</a>
</td>
<td>Called periodically during the sync operation to detect a request for cancellation.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>
</td>
<td>
<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-end">End</a>
</td>
<td>Called at the end of the operation.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>