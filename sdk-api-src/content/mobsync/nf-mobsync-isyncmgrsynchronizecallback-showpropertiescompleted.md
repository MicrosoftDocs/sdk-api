---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.ShowPropertiesCompleted
title: ISyncMgrSynchronizeCallback::ShowPropertiesCompleted
author: windows-sdk-content
description: Called by the registered application's handler before or after its ShowProperties operation is completed.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_showpropertiescompleted.htm
tech.root: shell
ms.assetid: d451e72e-d4a8-4899-b18e-d8912d817de5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],ShowPropertiesCompleted method, ISyncMgrSynchronizeCallback.ShowPropertiesCompleted, ISyncMgrSynchronizeCallback::ShowPropertiesCompleted, ShowPropertiesCompleted, ShowPropertiesCompleted method [Windows Shell], ShowPropertiesCompleted method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::ShowPropertiesCompleted, shell.syncmgr_isyncmgrsynchronizecallback_showpropertiescompleted, syncmgr.isyncmgrsynchronizecallback_showpropertiescompleted
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
 - ISyncMgrSynchronizeCallback.ShowPropertiesCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronizeCallback::ShowPropertiesCompleted


## -description


Called by the registered application's handler before or after its 
<a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> operation is completed.


## -parameters




### -param hr

TBD




#### - hrResult [in]

Type: <b>HRESULT</b>

Whether the <a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> was successful.


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
Call was completed successfully.

</td>
</tr>
</table>
 




## -remarks



It is acceptable for the registered application's handler to call this method before returning from the <a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> method.

This method should not be called if the registered application's handler does not return a success code from the <a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a>
 

 

