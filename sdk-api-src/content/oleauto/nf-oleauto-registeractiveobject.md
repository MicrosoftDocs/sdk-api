---
UID: NF:oleauto.RegisterActiveObject
title: RegisterActiveObject function (oleauto.h)
description: Registers an object as the active object for its class.
helpviewer_keywords: ["RegisterActiveObject","RegisterActiveObject function [Automation]","_oa96_RegisterActiveObject","automat.registeractiveobject","oleauto/RegisterActiveObject"]
old-location: automat\registeractiveobject.htm
tech.root: automat
ms.assetid: ba15bb69-7b65-47ea-b938-f235e3d9f9ee
ms.date: 12/05/2018
ms.keywords: RegisterActiveObject, RegisterActiveObject function [Automation], _oa96_RegisterActiveObject, automat.registeractiveobject, oleauto/RegisterActiveObject
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterActiveObject
 - oleauto/RegisterActiveObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - RegisterActiveObject
---

# RegisterActiveObject function


## -description

Registers an object as the active object for its class.

## -parameters

### -param punk

The active object.

### -param rclsid

The CLSID of the active object.

### -param dwFlags

Flags controlling registration of the object. Possible values are ACTIVEOBJECT_STRONG and ACTIVEOBJECT_WEAK.

### -param pdwRegister

Receives a handle. This handle must be passed to <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-revokeactiveobject">RevokeActiveObject</a> to end the object's active status.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>RegisterActiveObject</b> function registers the object to which <i>punk</i> points as the active object for the class denoted by <i>rclsid</i>. Registration causes the object to be listed in the running object table (ROT) of OLE, a globally accessible lookup table that keeps track of objects that are currently running on the computer. (For more information about the running object table, see the <i>COM Programmer's Reference</i>.) The <i>dwFlags</i> parameter specifies the strength or weakness of the registration, which affects the way the object is shut down.

In general, ActiveX objects should behave in the following manner:  

<ul>
<li>
If the object is visible, it should shut down only in response to an explicit user command (such as the <b>Exit</b> command on the <b>File</b> menu), or to the equivalent command from an ActiveX client (invoking the <b>Quit</b> or <b>Exit</b> method on the Application object).

</li>
<li>
If the object is not visible, it should shut down only when the last external connection to it is gone.

</li>
</ul>
Strong registration performs an <b>AddRef</b> on the object, incrementing the reference count of the object (and its associated stub) in the running object table. A strongly registered object must be explicitly revoked from the table with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-revokeactiveobject">RevokeActiveObject</a>. The default is strong registration (ACTIVEOBJECT_STRONG).

Weak registration keeps a pointer to the object in the running object table, but does not increment the reference count. Consequently, when the last external connection to a weakly registered object disappears, OLE releases the object's stub, and the object itself is no longer available.

To ensure the desired behavior, consider not only the default actions of OLE, but also the following:  

<ul>
<li>
Even though code can create an invisible object, the object may become visible at some later time. Once the object is visible, it should remain visible and active until it receives an explicit command to shut down. This can occur after references from the code disappear.

</li>
<li>
Other ActiveX clients may be using the object. If so, the code should not force the object to shut down.

</li>
</ul>
To avoid possible conflicts, you should always register ActiveX objects with ACTIVEOBJECT_WEAK, and call <b>CoLockObjectExternal</b>, when necessary, to guarantee the object remains active. <b>CoLockObjectExternal</b> adds a strong lock, thereby preventing the object's reference count from reaching zero. For detailed information about this function, refer to the <i>COM Programmer's Reference</i>.

Most commonly, objects need to call <b>CoLockObjectExternal</b> when they become visible, so they remain active until the user requests the object to shut down. The following procedure lists the steps your code should follow to shut down an object correctly.

<p class="proch"><b>To shut down an active object:</b>

<ol>
<li>
When the object becomes visible, make the following call to add a lock for user: 


```cpp
CoLockObjectExternal(punk, TRUE, TRUE)
```


The lock remains in effect until a user explicitly requests the object to be shut down, such as with a <b>Quit</b> or <b>Exit</b> command. 

</li>
<li>
When the user requests the object to be shut down, call <b>CoLockObjectExternal</b> again to free the lock, as follows: 


```cpp
CoLockObjectExternal(punk, FALSE, TRUE)
```


</li>
<li>
Call <b>RevokeActiveObject</b> to make the object inactive.

</li>
<li>
To end all connections from remote processes, call <b>CoDisconnectObject</b> as follows: 


```cpp
CoDisconnectObject(punk,0)
```


This function is described in more detail in the <i>COM Programmer's Reference</i>. 

</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/automat/registration-functions">Registering the Active Object with API Functions </a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-revokeactiveobject">RevokeActiveObject</a>