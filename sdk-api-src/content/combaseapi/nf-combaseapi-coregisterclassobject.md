---
UID: NF:combaseapi.CoRegisterClassObject
title: CoRegisterClassObject function
author: windows-sdk-content
description: Registers an EXE class object with OLE so other applications can connect to it.
old-location: com\coregisterclassobject.htm
tech.root: com
ms.assetid: d27bfa6c-194a-41f1-8fcf-76c4dff14a8a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CoRegisterClassObject, CoRegisterClassObject function [COM], _com_CoRegisterClassObject, com.coregisterclassobject, combaseapi/CoRegisterClassObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoRegisterClassObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoRegisterClassObject function


## -description


Registers an EXE class object with OLE so other applications can connect to it. 


## -parameters




### -param rclsid [in]

The CLSID to be registered.


### -param pUnk [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface on the class object whose availability is being published.


### -param dwClsContext [in]

The context in which the executable code is to be run. For information on these context values, see the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration.


### -param flags [in]

Indicates how connections are made to the class object. For information on these flags, see the <a href="https://msdn.microsoft.com/en-us/library/ms679697(v=VS.85).aspx">REGCLS</a> enumeration.


### -param lpdwRegister [out]

A pointer to a value that identifies the class object registered; later used by the <a href="https://msdn.microsoft.com/en-us/library/ms688650(v=VS.85).aspx">CoRevokeClassObject</a> function to revoke the registration.


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
Only EXE object applications call <b>CoRegisterClassObject</b>. Object handlers or DLL object applications do not call this function — instead, they must implement and export the <a href="https://msdn.microsoft.com/en-us/library/ms680760(v=VS.85).aspx">DllGetClassObject</a> function.

At startup, a multiple-use EXE object application must create a class object (with the <a href="https://msdn.microsoft.com/en-us/library/ms694364(v=VS.85).aspx">IClassFactory</a> interface on it), and call <b>CoRegisterClassObject</b> to register the class object. Object applications that support several different classes (such as multiple types of embeddable objects) must allocate and register a different class object for each.

Multiple registrations of the same class object are independent and do not produce an error. Each subsequent registration yields a unique key in <i>lpdwRegister</i>.

Multiple document interface (MDI) applications must register their class objects. Single document interface (SDI) applications must register their class objects only if they can be started by means of the <b>/Embedding</b> switch.

The server for a class object should call <a href="https://msdn.microsoft.com/en-us/library/ms688650(v=VS.85).aspx">CoRevokeClassObject</a> to revoke the class object (remove its registration) when all of the following are true:

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
After the class object is revoked, when its reference count reaches zero, the class object can be released, allowing the application to exit. Note that <b>CoRegisterClassObject</b> calls <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a> and <a href="https://msdn.microsoft.com/en-us/library/ms688650(v=VS.85).aspx">CoRevokeClassObject</a> calls <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a>, so the two functions form an <b>AddRef</b>/<b>Release</b> pair.



As of Windows Server 2003, if a COM object application is registered as a service, COM verifies the registration. COM makes sure the process ID of the service, in the service control manager (SCM), matches the process ID of the registering process. If not, COM fails the registration. If the COM object application runs in the system account with no registry key, COM treats the objects application identity as <a href="https://msdn.microsoft.com/en-us/library/ms693789(v=VS.85).aspx">Launching User</a>.




## -see-also




<a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688650(v=VS.85).aspx">CoRevokeClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680760(v=VS.85).aspx">DllGetClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms679697(v=VS.85).aspx">REGCLS</a>
 

 

