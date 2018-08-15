---
UID: NN:objidl.IRunnableObject
title: IRunnableObject
author: windows-sdk-content
description: Enables a container to control the running of its embedded objects.
old-location: com\irunnableobject.htm
old-project: com
ms.assetid: c682447b-5b12-41d5-a81d-fe94a117f740
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRunnableObject, IRunnableObject interface [COM], IRunnableObject interface [COM],described, _com_irunnableobject, com.irunnableobject, objidl/IRunnableObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunnableObject
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IRunnableObject interface


## -description


Enables a container to control the running of its embedded objects. In the case of an object implemented with a local server, calling the <a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">Run</a> method launches the server's .EXE file. In the case of an object implemented with an in-process server, calling <b>Run</b> causes the object .DLL file to transition into the running state.


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
<a href="https://msdn.microsoft.com/fb79e81c-0655-48ea-afb5-dab3529676d0">Run</a>
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

