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

# IGlobalInterfaceTable::RegisterInterfaceInGlobal


## -description


Registers the specified interface on an object residing in one apartment of a process as a global interface, enabling other apartments access to that interface.


## -parameters




### -param pUnk [in]

An interface pointer of type <i>riid</i> on the object on which the interface to be registered as global is implemented.


### -param riid [in]

The IID of the interface to be registered as global.


### -param pdwCookie [out]

An identifier that can be used by another apartment to get access to a pointer to the interface being registered. The value of an invalid cookie is 0.


## -returns



This method can return the following values.

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
The method completed successfully.

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
</table>
 




## -remarks



Called in the apartment in which an object resides to register one of the object's interfaces as a global interface. This method supplies a pointer to a cookie that other apartments can use in a call to the <a href="https://msdn.microsoft.com/3b37184d-c4e8-47b2-8f3f-008d3ea00759">GetInterfaceFromGlobal</a> method to get a pointer to that interface.

The interface pointer may be a pointer to an in-process object, or it may be a pointer to a proxy for an object residing in another apartment, in another process, or on another computer.

The apartment that calls this method must remain alive until the corresponding call to <a href="https://msdn.microsoft.com/202bf33a-5827-4cbf-b977-86167a9c633f">RevokeInterfaceFromGlobal</a>.




## -see-also




<a href="https://msdn.microsoft.com/0c1feee7-e33b-4b5d-8e35-4de6895e3947">IGlobalInterfaceTable</a>
 

 

