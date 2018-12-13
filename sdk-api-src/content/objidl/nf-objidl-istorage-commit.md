---
UID: NF:objidl.IStorage.Commit
title: IStorage::Commit
author: windows-sdk-content
description: The Commit method ensures that any changes made to a storage object open in transacted mode are reflected in the parent storage.
old-location: stg\istorage_commit.htm
tech.root: stg
ms.assetid: 72831f2c-1e07-429b-af4c-2aaced3f3888
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Commit, Commit method [Structured Storage], Commit method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],Commit method, IStorage.Commit, IStorage::Commit, _stg_istorage_commit, objidl/IStorage::Commit, stg.istorage_commit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IStorage.Commit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStorage::Commit


## -description


The <b>Commit</b> method ensures that any changes made to a storage object open in transacted mode are reflected in the parent storage. For nonroot storage objects in direct mode, this method has no effect. For a root storage, it reflects the changes in the actual device; for example, a file on disk. For a root storage object opened in direct mode, always call the <b>IStorage::Commit</b> method prior to <a href="_com_iunknown_release">Release</a>. <b>IStorage::Commit</b> flushes all memory buffers to the disk for a root storage in direct mode and will return an error code upon failure. Although <b>Release</b> also flushes memory buffers to disk, it has no capacity to return any error codes upon failure. Therefore, calling <b>Release</b> without first calling 
<b>Commit</b> causes indeterminate results.


## -parameters




### -param grfCommitFlags [in]

Controls how the changes are committed to the storage object. See the 
<a href="https://msdn.microsoft.com/f37260c0-d03d-4ead-a342-d2454ce8b1ac">STGC</a> enumeration for a definition of these values.


## -returns



This method can return one of these values.




## -remarks



<b>IStorage::Commit</b> makes permanent changes to a storage object that is in transacted mode, in which changes are accumulated in a buffer, and not reflected in the storage object until there is a call to this method. The alternative is to open an object in direct mode, in which changes are immediately reflected in the storage object. An object opened in the direct mode does not require calling <b>IStorage::Commit</b> to make permanent changes in the storage object. Calling the <b>IStorage::Commit</b> method on a nonroot storage opened in direct mode has no effect. Opening a root storage object in direct mode ensures that changes in memory buffers are written to the underlying storage device.

The commit operation publishes the current changes in this storage object and its children to the next level up in the storage hierarchy. To undo current changes before committing them, call <a href="https://msdn.microsoft.com/d1b7626e-bad1-47b5-8bcd-3da3b05c53c4">IStorage::Revert</a> to roll back to the last-committed version.

Calling <b>IStorage::Commit</b> has no effect on currently opened nested elements of this storage object. They remain valid and can be used. However, the <b>IStorage::Commit</b> method does not automatically commit changes to these nested elements. The commit operation publishes only known changes to the next higher level in the storage hierarchy. Thus, transactions to nested levels must be committed to this storage object before they can be committed to higher levels.

In commit operations, you need to take steps to ensure that data is protected during the commit process:

<ul>
<li>When committing changes to root storage objects, the caller must check the return value to determine whether the operation has been completed successfully, and if not, that the old committed contents of the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> are still intact and can be restored.</li>
<li>If this storage object was opened with some of its items excluded, the caller is responsible for rewriting them before calling commit. Write mode is required on the storage opening for the commit to succeed.</li>
<li>Unless prohibiting multiple simultaneous writers on the same storage object, an application calling this method should specify at least STGC_ONLYIFCURRENT in the <i>grfCommitFlags</i> parameter to prevent the changes made by one writer from inadvertently overwriting the changes made by another.</li>
</ul>
If the STGC_CONSOLIDATE flag is not supported by a storage implementation, calling <b>IStorage::Commit</b> with STGC_CONSOLIDATE specified in the <i>grfCommitFlags</i> parameter returns the value STG_E_INVALIDFLAG.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/d1b7626e-bad1-47b5-8bcd-3da3b05c53c4">IStorage::Revert</a>



<a href="https://msdn.microsoft.com/f37260c0-d03d-4ead-a342-d2454ce8b1ac">STGC</a>
 

 

