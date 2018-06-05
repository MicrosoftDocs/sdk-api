---
UID: NF:combaseapi.CoRegisterClassObject
title: CoRegisterClassObject function
author: windows-sdk-content
description: Registers an EXE class object with OLE so other applications can connect to it.
old-location: com\coregisterclassobject.htm
old-project: com
ms.assetid: d27bfa6c-194a-41f1-8fcf-76c4dff14a8a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CoRegisterClassObject, CoRegisterClassObject function [COM], _com_CoRegisterClassObject, com.coregisterclassobject, combaseapi/CoRegisterClassObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
req.typenames: REGCLS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	API-MS-Win-Core-Com-l1-1-0.dll
-	ComBase.dll
-	API-MS-Win-Core-Com-l1-1-1.dll
-	API-MS-Win-DownLevel-Ole32-l1-1-0.dll
-	API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
-	CoRegisterClassObject
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoRegisterClassObject function


## -description


Registers an EXE class object with OLE so other applications can connect to it. 


## -parameters




### -param rclsid [in]

The CLSID to be registered.


### -param pUnk [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on the class object whose availability is being published.


### -param dwClsContext [in]

The context in which the executable code is to be run. For information on these context values, see the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration.


### -param flags [in]

Indicates how connections are made to the class object. For information on these flags, see the <a href="https://msdn.microsoft.com/16bca8e0-9999-4d51-b7f0-87deb7619d89">REGCLS</a> enumeration.


### -param lpdwRegister [out]

A pointer to a value that identifies the class object registered; later used by the <a href="https://msdn.microsoft.com/90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec">CoRevokeClassObject</a> function to revoke the registration.


## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The class object was registered successfully.

</td>
</tr>
</table>
 




## -remarks



EXE object applications should call <b>CoRegisterClassObject</b> on startup. It can also be used to register internal objects for use by the same EXE or other code (such as DLLs) that the EXE uses.
Only EXE object applications call <b>CoRegisterClassObject</b>. Object handlers or DLL object applications do not call this function — instead, they must implement and export the <a href="https://msdn.microsoft.com/42c08149-c251-47f7-a81f-383975d7081c">DllGetClassObject</a> function.

At startup, a multiple-use EXE object application must create a class object (with the <a href="https://msdn.microsoft.com/f624f833-2b69-43bc-92cd-c4ecbe6051c5">IClassFactory</a> interface on it), and call <b>CoRegisterClassObject</b> to register the class object. Object applications that support several different classes (such as multiple types of embeddable objects) must allocate and register a different class object for each.

Multiple registrations of the same class object are independent and do not produce an error. Each subsequent registration yields a unique key in <i>lpdwRegister</i>.

Multiple document interface (MDI) applications must register their class objects. Single document interface (SDI) applications must register their class objects only if they can be started by means of the <b>/Embedding</b> switch.

The server for a class object should call <a href="https://msdn.microsoft.com/90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec">CoRevokeClassObject</a> to revoke the class object (remove its registration) when all of the following are true:

<ul>
<li>
There are no existing instances of the object definition.

</li>
<li>
There are no locks on the class object.

</li>
<li>
The application providing services to the class object is not under user control (not visible to the user on the display).

</li>
</ul>
After the class object is revoked, when its reference count reaches zero, the class object can be released, allowing the application to exit. Note that <b>CoRegisterClassObject</b> calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> and <a href="https://msdn.microsoft.com/90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec">CoRevokeClassObject</a> calls <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>, so the two functions form an <b>AddRef</b>/<b>Release</b> pair.



As of Windows Server 2003, if a COM object application is registered as a service, COM verifies the registration. COM makes sure the process ID of the service, in the service control manager (SCM), matches the process ID of the registering process. If not, COM fails the registration. If the COM object application runs in the system account with no registry key, COM treats the objects application identity as <a href="https://msdn.microsoft.com/ea5140b6-0a79-4149-b845-4f6388e89104">Launching User</a>.




## -see-also




<a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>



<a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec">CoRevokeClassObject</a>



<a href="https://msdn.microsoft.com/42c08149-c251-47f7-a81f-383975d7081c">DllGetClassObject</a>



<a href="https://msdn.microsoft.com/16bca8e0-9999-4d51-b7f0-87deb7619d89">REGCLS</a>
 

 

