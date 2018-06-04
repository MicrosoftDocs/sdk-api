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

# IWbemBackupRestoreEx::Resume


## -description


The <b>IWbemBackUpRestoreEx::Resume</b> method releases a lock on the Windows Management Instrumentation (WMI) repository so  operations can continue.


## -parameters






## -returns



This method returns an <b>HRESULT</b> that indicates the status of a method call. The following list lists the values contained within an <b>HRESULT</b>.




## -remarks



The <b>Resume</b> method should always be called when the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a> method is called. <b>Resume</b> must be called on the same instance of <a href="https://msdn.microsoft.com/5349359a-e15f-4799-abad-f4a5fc3e89ea">IWbemBackUpRestoreEx</a> that the <b>Pause</b> method is implemented. Releasing the object without calling <b>Resume</b> automatically causes the <b>Resume</b> method to be implemented.

<div class="alert"><b>Note</b>  To implement the <b>Resume</b> method, the client user must have <b>SE_BACKUP_NAME</b> prior to calling the method.</div>
<div> </div>

#### Examples

The following C++ example shows how to call the <b>IWbemBackUpRestoreEx::Resume</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// The pInt variable is of type IWbemBackupRestoreEx*
pInt-&gt;Resume();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5349359a-e15f-4799-abad-f4a5fc3e89ea">IWbemBackupRestoreEx</a>
 

 

