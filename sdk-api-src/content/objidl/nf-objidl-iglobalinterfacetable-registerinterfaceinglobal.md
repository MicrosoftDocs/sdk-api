---
UID: NF:objidl.IGlobalInterfaceTable.RegisterInterfaceInGlobal
title: IGlobalInterfaceTable::RegisterInterfaceInGlobal
author: windows-sdk-content
description: Registers the specified interface on an object residing in one apartment of a process as a global interface, enabling other apartments access to that interface.
old-location: com\iglobalinterfacetable_registerinterfaceinglobal.htm
old-project: com
ms.assetid: 5282b0b8-4eab-4114-8061-6d74db3756b7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IGlobalInterfaceTable interface [COM],RegisterInterfaceInGlobal method, IGlobalInterfaceTable.RegisterInterfaceInGlobal, IGlobalInterfaceTable::RegisterInterfaceInGlobal, RegisterInterfaceInGlobal, RegisterInterfaceInGlobal method [COM], RegisterInterfaceInGlobal method [COM],IGlobalInterfaceTable interface, _com_iglobalinterfacetable_registerinterfaceinglobal, com.iglobalinterfacetable_registerinterfaceinglobal, objidlbase/IGlobalInterfaceTable::RegisterInterfaceInGlobal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalInterfaceTable.RegisterInterfaceInGlobal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

