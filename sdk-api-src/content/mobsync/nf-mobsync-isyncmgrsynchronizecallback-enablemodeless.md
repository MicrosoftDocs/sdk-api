---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.EnableModeless
title: ISyncMgrSynchronizeCallback::EnableModeless
author: windows-sdk-content
description: Called by the registered application before and after any dialog boxes are displayed from within the PrepareForSync and Synchronize methods.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_enablemodeless.htm
old-project: shell
ms.assetid: 00102220-3734-40f2-ae6c-2807e44e17a1
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: EnableModeless, EnableModeless method [Windows Shell], EnableModeless method [Windows Shell],ISyncMgrSynchronizeCallback interface, ISyncMgrSynchronizeCallback interface [Windows Shell],EnableModeless method, ISyncMgrSynchronizeCallback.EnableModeless, ISyncMgrSynchronizeCallback::EnableModeless, mobsync/ISyncMgrSynchronizeCallback::EnableModeless, shell.syncmgr_isyncmgrsynchronizecallback_enablemodeless, syncmgr.isyncmgrsynchronizecallback_enablemodeless
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeCallback.EnableModeless
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronizeCallback::EnableModeless


## -description


Called by the registered application before and after any dialog boxes are displayed from within the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> and 
<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> methods.


## -parameters




### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> if the registered application is requesting permission to display a dialog box or <b>FALSE</b> if the registered application has finished displaying a dialog box.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
Continue the synchronization.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The dialog box should not be displayed.

</td>
</tr>
</table>
 




## -remarks



To request permission to display a dialog box, the registered application first calls <b>ISyncMgrSynchronizeCallback::EnableModeless</b> with <i>fEnable</i> set to <b>TRUE</b>. If S_OK is returned, the registered application may display the dialog box. Once the dialog box has been displayed, the registered application must call <b>ISyncMgrSynchronizeCallback::EnableModeless</b> with <i>fEnable</i> set to <b>FALSE</b> to notify SyncMgr that other items may now display user interface elements.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a>



<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a>
 

 

