---
UID: NF:combaseapi.CoRevokeClassObject
title: CoRevokeClassObject function (combaseapi.h)
description: Informs OLE that a class object, previously registered with the CoRegisterClassObject function, is no longer available for use.
helpviewer_keywords: ["CoRevokeClassObject","CoRevokeClassObject function [COM]","_com_CoRevokeClassObject","com.corevokeclassobject","combaseapi/CoRevokeClassObject"]
old-location: com\corevokeclassobject.htm
tech.root: com
ms.assetid: 90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec
ms.date: 12/05/2018
ms.keywords: CoRevokeClassObject, CoRevokeClassObject function [COM], _com_CoRevokeClassObject, com.corevokeclassobject, combaseapi/CoRevokeClassObject
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
 - CoRevokeClassObject
 - combaseapi/CoRevokeClassObject
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
 - CoRevokeClassObject
---

# CoRevokeClassObject function


## -description

Informs OLE that a class object, previously registered with the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a> function, is no longer available for use.

## -parameters

### -param dwRegister [in]

A token previously returned from the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a> function.

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

A successful call to <b>CoRevokeClassObject</b> means that the class object has been removed from the global class object table (although it does not release the class object). If other clients still have pointers to the class object and have caused the reference count to be incremented by calls to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>, the reference count will not be zero. When this occurs, applications may benefit if subsequent calls (with the obvious exceptions of <b>AddRef</b> and <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>) to the class object fail. Note that <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a> calls <b>AddRef</b> and <b>CoRevokeClassObject</b> calls <b>Release</b>, so the two functions form an <b>AddRef</b>/<b>Release</b> pair.



An object application must call <b>CoRevokeClassObject</b> to revoke registered class objects before exiting the program. Class object implementers should call <b>CoRevokeClassObject</b> as part of the release sequence. You must specifically revoke the class object even when you have specified the flags value REGCLS_SINGLEUSE in a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>, indicating that only one application can connect to the class object.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>