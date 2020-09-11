---
UID: NN:objidl.IRunnableObject
title: IRunnableObject (objidl.h)
description: Enables a container to control the running of its embedded objects.
helpviewer_keywords: ["IRunnableObject","IRunnableObject interface [COM]","IRunnableObject interface [COM]","described","_com_irunnableobject","com.irunnableobject","objidl/IRunnableObject"]
old-location: com\irunnableobject.htm
tech.root: com
ms.assetid: c682447b-5b12-41d5-a81d-fe94a117f740
ms.date: 12/05/2018
ms.keywords: IRunnableObject, IRunnableObject interface [COM], IRunnableObject interface [COM],described, _com_irunnableobject, com.irunnableobject, objidl/IRunnableObject
req.header: objidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRunnableObject
 - objidl/IRunnableObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunnableObject
---

# IRunnableObject interface


## -description

Enables a container to control the running of its embedded objects. In the case of an object implemented with a local server, calling the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-run">Run</a> method launches the server's .EXE file. In the case of an object implemented with an in-process server, calling <b>Run</b> causes the object .DLL file to transition into the running state.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRunnableObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRunnableObject</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-getrunningclass">GetRunningClass</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of a running object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-isrunning">IsRunning</a>
</td>
<td align="left" width="63%">
Determines whether an object is currently in the running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-lockrunning">LockRunning</a>
</td>
<td align="left" width="63%">
Locks an already running object into its running state or unlocks it from its running state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-run">Run</a>
</td>
<td align="left" width="63%">
Forces an object to run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-setcontainedobject">SetContainedObject</a>
</td>
<td align="left" width="63%">
Notifies an object that it is embedded in an OLE container.

</td>
</tr>
</table>

