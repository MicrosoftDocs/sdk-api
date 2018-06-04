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

# IRunnableObject interface


## -description


Enables a container to control the running of its embedded objects. In the case of an object implemented with a local server, calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a> method launches the server's .EXE file. In the case of an object implemented with an in-process server, calling <b>Run</b> causes the object .DLL file to transition into the running state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRunnableObject</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IRunnableObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRunnableObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfe80741-ceda-44cd-8506-1807bb664ad0">GetRunningClass</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of a running object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a4cdd21-8256-4533-9cad-d9e8450a17e9">IsRunning</a>
</td>
<td align="left" width="63%">
Determines whether an object is currently in the running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce501785-16ad-4120-abea-41e2d6ca67df">LockRunning</a>
</td>
<td align="left" width="63%">
Locks an already running object into its running state or unlocks it from its running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a>
</td>
<td align="left" width="63%">
Forces an object to run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbd3f632-2b81-44d1-8376-4b507316895f">SetContainedObject</a>
</td>
<td align="left" width="63%">
Notifies an object that it is embedded in an OLE container.

</td>
</tr>
</table> 

