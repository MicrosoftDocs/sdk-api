---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.DeleteLogError
title: ISyncMgrSynchronizeCallback::DeleteLogError
author: windows-driver-content
description: Called by the registered application's handler to delete a previously logged ErrorInformation, warning, or error message in the error tab on the synchronization manager status dialog box.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_deletelogerror.htm
old-project: shell
ms.assetid: 06e90b81-14cc-4b3e-9d2d-30e60eeb8eb2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DeleteLogError, DeleteLogError method [Windows Shell], DeleteLogError method [Windows Shell],ISyncMgrSynchronizeCallback interface, ISyncMgrSynchronizeCallback interface [Windows Shell],DeleteLogError method, ISyncMgrSynchronizeCallback.DeleteLogError, ISyncMgrSynchronizeCallback::DeleteLogError, mobsync/ISyncMgrSynchronizeCallback::DeleteLogError, shell.syncmgr_isyncmgrsynchronizecallback_deletelogerror, syncmgr.isyncmgrsynchronizecallback_deletelogerror
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
req.typenames: SYNCMGRSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mobsync.dll
api_name:
-	ISyncMgrSynchronizeCallback.DeleteLogError
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronizeCallback::DeleteLogError


## -description


Called by the registered application's handler to delete a previously logged ErrorInformation, warning, or error message in the error tab on the synchronization manager status dialog box.


## -parameters




### -param ErrorID [in]

Type: <b>REFGUID</b>

The LogError to be deleted. If <i>ErrorID</i> is GUID_NULL all errors logged by the instance of the registered application's handler will be deleted.


### -param dwReserved [in]

Type: <b>DWORD</b>


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, as well as the following:

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
The item was successfully deleted from the log.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>
 

 

