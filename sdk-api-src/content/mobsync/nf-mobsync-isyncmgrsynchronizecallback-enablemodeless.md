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
 

 

