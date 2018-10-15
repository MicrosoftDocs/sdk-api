---
UID: NF:mobsync.ISyncMgrSynchronize.PrepareForSync
title: ISyncMgrSynchronize::PrepareForSync
author: windows-sdk-content
description: Allows a registered application to display any user interface, and perform any necessary initialization before the ISyncMgrSynchronize::Synchronize method is called.
old-location: shell\syncmgr_isyncmgrsynchronize_prepareforsync.htm
tech.root: shell
ms.assetid: 82e70e75-a5d4-41b2-87c4-2a032628954d
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],PrepareForSync method, ISyncMgrSynchronize.PrepareForSync, ISyncMgrSynchronize::PrepareForSync, PrepareForSync, PrepareForSync method [Windows Shell], PrepareForSync method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::PrepareForSync, shell.syncmgr_isyncmgrsynchronize_prepareforsync, syncmgr.isyncmgrsynchronize_prepareforsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Mobsync.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronize.PrepareForSync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronize::PrepareForSync


## -description


Allows a registered application to display any user interface, and perform any necessary initialization before the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> method is called. For example, an application such as the Microsoft Outlook email client may need to display the password dialog box to enable a user to log on to a mail server.


## -parameters




### -param cbNumItems [in]

Type: <b>ULONG</b>

The number of items in the array pointed to by <i>pItemIDs</i>.


### -param pItemIDs [in]

Type: <b>GUID*</b>

An array of item IDs that a user chooses to synchronize.


### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent <b>HWND</b> that a registered application should use for any user interface element displayed. This value may be <b>NULL</b>.


### -param dwReserved [in]

Type: <b>DWORD</b>

Reserved. Registered applications should ignore this value.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Preparation is successful.

</td>
</tr>
</table>
 




## -remarks



A registered application handler should return from this method as soon as possible, and then call the <a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">PrepareForSyncCompleted</a> method. A registered application handler can call the <b>PrepareForSyncCompleted</b> method before returning from this method.

Registered applications should only show a user interface if the 
<a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is set in the <i>dwSyncFlags</i> parameter of the 
<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a> method. If a registered application cannot prepare for synchronization without showing a user interface when the <a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is not set, it should return S_FALSE from this method.

The array of item IDs that are passed into this method are relevant to the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> method also.

The <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> methods can be called on any thread in a registered application.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a>



<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a>



<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">PrepareForSyncCompleted</a>



<a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG</a>
 

 

