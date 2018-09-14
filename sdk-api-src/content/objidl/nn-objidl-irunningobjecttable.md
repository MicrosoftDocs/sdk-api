---
UID: NN:objidl.IRunningObjectTable
title: IRunningObjectTable
author: windows-sdk-content
description: Manages access to the running object table (ROT), a globally accessible look-up table on each workstation.
old-location: com\irunningobjecttable.htm
tech.root: com
ms.assetid: ff89bcb5-df6d-4325-b0e8-613217a68f42
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IRunningObjectTable, IRunningObjectTable interface [COM], IRunningObjectTable interface [COM],described, _com_irunningobjecttable, com.irunningobjecttable, objidl/IRunningObjectTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunningObjectTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRunningObjectTable interface


## -description


Manages access to the running object table (ROT), a globally accessible look-up table on each workstation. A workstation's ROT keeps track of those objects that can be identified by a moniker and that are currently running on the workstation. When a client tries to bind a moniker to an object, the moniker checks the ROT to see if the object is already running; this allows the moniker to bind to the current instance instead of loading a new one.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRunningObjectTable</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IRunningObjectTable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRunningObjectTable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09ff0d05-627b-4e47-8534-25cd8735c6e5">EnumRunning</a>
</td>
<td align="left" width="63%">
Creates and returns a pointer to an enumerator that can list the monikers of all the objects currently registered in the running object table (ROT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d74b3ee-323d-43f9-8eab-0866432659de">GetObject</a>
</td>
<td align="left" width="63%">
Determines whether the object identified by the specified moniker is running, and if it is, retrieves a pointer to that object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fef6f7e5-7d91-4737-98a4-c9779c6c2be5">GetTimeOfLastChange</a>
</td>
<td align="left" width="63%">
Retrieves the time that an object was last modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44564e70-b157-4f60-9b51-337613f6a4c9">IsRunning</a>
</td>
<td align="left" width="63%">
Determines whether the object identified by the specified moniker is currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bc410f8-3a39-478d-bc4d-adcd976f305b">NoteChangeTime</a>
</td>
<td align="left" width="63%">
Records the time that a running object was last modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">Register</a>
</td>
<td align="left" width="63%">
Registers an object and its identifying moniker in the running object table (ROT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3d83966-035d-4077-a770-cb62c8011132">Revoke</a>
</td>
<td align="left" width="63%">
Removes an entry from the running object table (ROT) that was previously registered by a call to <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a>.

</td>
</tr>
</table> 


## -remarks



The ROT contains entries of the following form: (<i>pmkObjectName</i>, <i>pUnkObject</i>).

The <i>pmkObjectName</i> element is a pointer to the moniker that identifies the running object. The <i>pUnkObject</i> element is a pointer to the running object itself. During the binding process, monikers consult the <i>pmkObjectName</i> entries in the ROT to see whether an object is already running.

Objects that can be named by monikers must be registered with the ROT when they are loaded and their registration must be revoked when they are no longer running.




## -see-also




<a href="https://msdn.microsoft.com/65d9cf7d-cc8a-4199-9a4a-7fd67ef8872d">GetRunningObjectTable</a>



<a href="https://msdn.microsoft.com/26938d07-d772-4e72-a6aa-57dd2f2cece1">IBindCtx::GetRunningObjectTable</a>



<a href="https://msdn.microsoft.com/44ae8377-c375-4dc3-9f54-a5674e24763f">IROTData</a>
 

 

