---
UID: NF:objbase.CoRevokeMallocSpy
title: CoRevokeMallocSpy function (objbase.h)
author: windows-sdk-content
description: Revokes a registered IMallocSpy object.
old-location: com\corevokemallocspy.htm
tech.root: com
ms.assetid: e1e984a2-2aee-452c-840c-42201ef5ee96
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoRevokeMallocSpy, CoRevokeMallocSpy function [COM], _com_CoRevokeMallocSpy, com.corevokemallocspy, objbase/CoRevokeMallocSpy
ms.topic: function
f1_keywords: ["objbase/CoRevokeMallocSpy"]
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoRevokeMallocSpy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoRevokeMallocSpy function


## -description


Revokes a registered <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> object.




## -parameters






## -returns



This function can return the following values.

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
The object was revoked successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_OBJNOTREG</b></dt>
</dl>
</td>
<td width="60%">
No spy is currently registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
A spy is registered but there are outstanding allocations (not yet freed) made while this spy was active.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> object is released when it is revoked. This release corresponds to the call to <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> in the implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> function by the <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a> function. The implementation of the <b>IMallocSpy</b> interface should then do any appropriate cleanup.



If the return code is E_ACCESSDENIED, there are still outstanding allocations that were made while the spy was active. In this case, the registered spy cannot be revoked at this time because it may have attached arbitrary headers and/or trailers to these allocations that only the spy knows about. Only the spy's <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-prefree">PreFree</a> (or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imallocspy-prerealloc">PreRealloc</a>) method knows how to account for these headers and trailers. Before returning E_ACCESSDENIED, <b>CoRevokeMallocSpy</b> notes internally that a revoke is pending. When the outstanding allocations have been freed, the revoke proceeds automatically, releasing the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> object. Thus, it is necessary to call <b>CoRevokeMallocSpy</b> only once for each call to <a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a>, even if E_ACCESSDENIED is returned.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coregistermallocspy">CoRegisterMallocSpy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>
 

 

