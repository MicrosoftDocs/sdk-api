---
UID: NF:ole2.OleLockRunning
title: OleLockRunning function
author: windows-sdk-content
description: Locks an already running object into its running state or unlocks it from its running state.
old-location: com\olelockrunning.htm
old-project: com
ms.assetid: 84941a59-6880-4824-b4b9-cd1b52d2bffb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OleLockRunning, OleLockRunning function [COM], _ole_OleLockRunning, com.olelockrunning, ole2/OleLockRunning
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
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
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleLockRunning
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleLockRunning function


## -description


Locks an already running object into its running state or unlocks it from its running state.




## -parameters




### -param pUnknown [in]

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the object, which the function uses to query for a pointer to <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a>.


### -param fLock [in]

<b>TRUE</b> locks the object into its running state. <b>FALSE</b> unlocks the object from its running state.


### -param fLastUnlockCloses [in]

<b>TRUE</b> specifies that if the connection being released is the last external lock on the object, the object should close. <b>FALSE</b> specifies that the object should remain open until closed by the user or another process.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



The <b>OleLockRunning</b> function saves you the trouble of calling the <a href="https://msdn.microsoft.com/ce501785-16ad-4120-abea-41e2d6ca67df">IRunnableObject::LockRunning</a> method. You can use <b>OleLockRunning</b> and <b>IRunnableObject::LockRunning</b> interchangeably. With the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer passed in with the <i>pUnknown</i> parameter, <b>OleLockRunning</b> queries for an <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> pointer. If successful, it calls <b>IRunnableObject::LockRunning</b> and returns the results of the call.



For more information on using this function, see <a href="https://msdn.microsoft.com/ce501785-16ad-4120-abea-41e2d6ca67df">IRunnableObject::LockRunning</a>.




## -see-also




<a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a>



<a href="https://msdn.microsoft.com/ce501785-16ad-4120-abea-41e2d6ca67df">IRunnableObject::LockRunning</a>



<a href="https://msdn.microsoft.com/f140f068-3115-4389-b67b-6d41d12f7525">OleNoteObjectVisible</a>
 

 

