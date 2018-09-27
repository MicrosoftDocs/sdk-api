---
UID: NF:combaseapi.CoRevokeClassObject
title: CoRevokeClassObject function
author: windows-sdk-content
description: Informs OLE that a class object, previously registered with the CoRegisterClassObject function, is no longer available for use.
old-location: com\corevokeclassobject.htm
tech.root: com
ms.assetid: 90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CoRevokeClassObject, CoRevokeClassObject function [COM], _com_CoRevokeClassObject, com.corevokeclassobject, combaseapi/CoRevokeClassObject
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
 - CoRevokeClassObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoRevokeClassObject function


## -description


Informs OLE that a class object, previously registered with the <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a> function, is no longer available for use.


## -parameters




### -param dwRegister [in]

A token previously returned from the <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a> function.


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
The class object was revoked successfully.

</td>
</tr>
</table>
 




## -remarks



A successful call to <b>CoRevokeClassObject</b> means that the class object has been removed from the global class object table (although it does not release the class object). If other clients still have pointers to the class object and have caused the reference count to be incremented by calls to <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a>, the reference count will not be zero. When this occurs, applications may benefit if subsequent calls (with the obvious exceptions of <b>AddRef</b> and <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a>) to the class object fail. Note that <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a> calls <b>AddRef</b> and <b>CoRevokeClassObject</b> calls <b>Release</b>, so the two functions form an <b>AddRef</b>/<b>Release</b> pair.



An object application must call <b>CoRevokeClassObject</b> to revoke registered class objects before exiting the program. Class object implementers should call <b>CoRevokeClassObject</b> as part of the release sequence. You must specifically revoke the class object even when you have specified the flags value REGCLS_SINGLEUSE in a call to <a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a>, indicating that only one application can connect to the class object.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684007(v=VS.85).aspx">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693407(v=VS.85).aspx">CoRegisterClassObject</a>
 

 

