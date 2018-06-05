---
UID: NF:mobsync.ISyncMgrSynchronize.ShowError
title: ISyncMgrSynchronize::ShowError
author: windows-sdk-content
description: Called by the synchronization manager in a registered application handler when a user double-clicks an associated message in the error tab.
old-location: shell\syncmgr_isyncmgrsynchronize_showerror.htm
old-project: shell
ms.assetid: 0e313c61-6482-4396-b4b8-824fba0226ac
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],ShowError method, ISyncMgrSynchronize.ShowError, ISyncMgrSynchronize::ShowError, ShowError, ShowError method [Windows Shell], ShowError method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::ShowError, shell.syncmgr_isyncmgrsynchronize_showerror, syncmgr.isyncmgrsynchronize_showerror
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGRSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mobsync.dll
api_name:
-	ISyncMgrSynchronize.ShowError
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronize::ShowError


## -description


Called by the synchronization manager in a registered application handler when a user double-clicks an associated message in the error tab.


## -parameters




### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent <b>HWND</b> that a registered application should use to display a user interface. This value can be <b>NULL</b>.


### -param ErrorID [in]

Type: <b>REFGUID</b>

An error identifier that is associated with this error message. This value is passed in the <a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">LogError</a> method.


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
The call is completed successfully.

</td>
</tr>
</table>
 




## -remarks



Handlers should return as soon as possible from this method, and call the <a href="https://msdn.microsoft.com/7441f8d3-1b9b-400f-a2c4-ec67f7677a32">ShowErrorCompleted</a> method. A handler can make a call to 
<b>ShowErrorCompleted</b> before returning from this method. If a handler returns a failure code from this method, it should not call the 
<b>ShowErrorCompleted</b> method.

Applications can display user interface elements in this method even if the 
<a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is not set in the <i>dwSyncFlags</i> parameter of the 
<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a> method. Applications must still call <a href="https://msdn.microsoft.com/00102220-3734-40f2-ae6c-2807e44e17a1">EnableModeless</a>, and check the return code before showing a user interface.




## -see-also




<a href="https://msdn.microsoft.com/00102220-3734-40f2-ae6c-2807e44e17a1">EnableModeless</a>



<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a>



<a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">LogError</a>



<a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG</a>



<a href="https://msdn.microsoft.com/7441f8d3-1b9b-400f-a2c4-ec67f7677a32">ShowErrorCompleted</a>
 

 

