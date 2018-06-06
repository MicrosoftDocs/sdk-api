---
UID: NF:oleidl.IOleContainer.LockContainer
title: IOleContainer::LockContainer
author: windows-sdk-content
description: Keeps the container for embedded objects running until explicitly released.
old-location: com\iolecontainer_lockcontainer.htm
old-project: com
ms.assetid: 31b9961a-29a2-48bf-9d39-d86718983682
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IOleContainer interface [COM],LockContainer method, IOleContainer.LockContainer, IOleContainer::LockContainer, LockContainer, LockContainer method [COM], LockContainer method [COM],IOleContainer interface, _ole_iolecontainer_lockcontainer, com.iolecontainer_lockcontainer, oleidl/IOleContainer::LockContainer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleContainer.LockContainer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleContainer::LockContainer


## -description


Keeps the container for embedded objects running until explicitly released.


## -parameters




### -param fLock [in]

Indicates whether to lock (<b>TRUE</b>) or unlock (<b>FALSE</b>) a container.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for the operation.

</td>
</tr>
</table>
 




## -remarks



An embedded object calls <b>LockContainer</b> to keep its container running when the object has link clients that require an update. If an end user selects <b>File Close</b> from the container's menu, however, the container ignores all outstanding <b>LockContainer</b> locks and closes the document anyway.




## -see-also




<a href="https://msdn.microsoft.com/36eb55f1-06de-49ad-8a8d-91693ca92e99">CoLockObjectExternal</a>



<a href="https://msdn.microsoft.com/98549309-8ac8-4391-92ab-8a62269ff579">IOleContainer</a>



<a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">IRunnableObject::Run</a>
 

 

