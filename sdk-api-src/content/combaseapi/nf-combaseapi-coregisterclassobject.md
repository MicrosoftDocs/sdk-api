---
UID: NF:combaseapi.CoRegisterClassObject
title: CoRegisterClassObject function (combaseapi.h)
description: Registers an EXE class object with OLE so other applications can connect to it.
helpviewer_keywords: ["CoRegisterClassObject","CoRegisterClassObject function [COM]","_com_CoRegisterClassObject","com.coregisterclassobject","combaseapi/CoRegisterClassObject"]
old-location: com\coregisterclassobject.htm
tech.root: com
ms.assetid: d27bfa6c-194a-41f1-8fcf-76c4dff14a8a
ms.date: 12/05/2018
ms.keywords: CoRegisterClassObject, CoRegisterClassObject function [COM], _com_CoRegisterClassObject, com.coregisterclassobject, combaseapi/CoRegisterClassObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoRegisterClassObject
 - combaseapi/CoRegisterClassObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoRegisterClassObject
---

# CoRegisterClassObject function


## -description

Registers an EXE class object with OLE so other applications can connect to it.

## -parameters

### -param rclsid [in]

The CLSID to be registered.

### -param pUnk [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the class object whose availability is being published.

### -param dwClsContext [in]

The context in which the executable code is to be run. For information on these context values, see the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> enumeration.

### -param flags [in]

Indicates how connections are made to the class object. For information on these flags, see the <a href="/windows/desktop/api/combaseapi/ne-combaseapi-regcls">REGCLS</a> enumeration.

### -param lpdwRegister [out]

A pointer to a value that identifies the class object registered; later used by the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> function to revoke the registration.

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
Only EXE object applications call <b>CoRegisterClassObject</b>. Object handlers or DLL object applications do not call this function — instead, they must implement and export the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject">DllGetClassObject</a> function.

At startup, a multiple-use EXE object application must create a class object (with the <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> interface on it), and call <b>CoRegisterClassObject</b> to register the class object. Object applications that support several different classes (such as multiple types of embeddable objects) must allocate and register a different class object for each.

Multiple registrations of the same class object are independent and do not produce an error. Each subsequent registration yields a unique key in <i>lpdwRegister</i>.

Multiple document interface (MDI) applications must register their class objects. Single document interface (SDI) applications must register their class objects only if they can be started by means of the <b>/Embedding</b> switch.

The server for a class object should call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> to revoke the class object (remove its registration) when all of the following are true:

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
After the class object is revoked, when its reference count reaches zero, the class object can be released, allowing the application to exit. Note that <b>CoRegisterClassObject</b> calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>, so the two functions form an <b>AddRef</b>/<b>Release</b> pair.



As of Windows Server 2003, if a COM object application is registered as a service, COM verifies the registration. COM makes sure the process ID of the service, in the service control manager (SCM), matches the process ID of the registering process. If not, COM fails the registration. If the COM object application runs in the system account with no registry key, COM treats the objects application identity as <a href="/windows/desktop/com/launching-user">Launching User</a>.

## -see-also

<a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject">DllGetClassObject</a>



<a href="/windows/desktop/api/combaseapi/ne-combaseapi-regcls">REGCLS</a>