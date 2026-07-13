---
UID: NF:objbase.CoRegisterMallocSpy
title: CoRegisterMallocSpy function (objbase.h)
description: Registers an implementation of the IMallocSpy interface, thereafter requiring OLE to call its wrapper methods around every call to the corresponding IMalloc method.
helpviewer_keywords: ["CoRegisterMallocSpy","CoRegisterMallocSpy function [COM]","_com_CoRegisterMallocSpy","com.coregistermallocspy","objbase/CoRegisterMallocSpy"]
old-location: com\coregistermallocspy.htm
tech.root: com
ms.assetid: 28623c1f-e158-4cc5-8c7f-c13d7a65aa76
ms.date: 12/05/2018
ms.keywords: CoRegisterMallocSpy, CoRegisterMallocSpy function [COM], _com_CoRegisterMallocSpy, com.coregistermallocspy, objbase/CoRegisterMallocSpy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoRegisterMallocSpy
 - objbase/CoRegisterMallocSpy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-private-l1-3-1.dll
 - api-ms-win-core-com-private-l1-3-0.dll
 - api-ms-win-core-com-private-l1-2-0.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoRegisterMallocSpy
---

# CoRegisterMallocSpy function


## -description

Registers an implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> interface, thereafter requiring OLE to call its wrapper methods around every call to the corresponding <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> method.

## -parameters

### -param pMallocSpy [in]

A pointer to an instance of the <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> implementation.

## -returns

This function can return the standard return value E_INVALIDARG, as well as the following values.

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
The object was successfully registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_OBJISREG</b></dt>
</dl>
</td>
<td width="60%">
The object is already registered.

</td>
</tr>
</table>

## -remarks

The <b>CoRegisterMallocSpy</b> function registers the <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> object, which is used to debug calls to <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> methods. The function calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the pointer <i>pMallocSpy</i> for the interface IID_IMallocSpy. This is to ensure that <i>pMallocSpy</i> really points to an implementation of <b>IMallocSpy</b>. By the rules of OLE, it is expected that a successful call to <b>QueryInterface</b> has added a reference (through the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method) to the <b>IMallocSpy</b> object. That is, <b>CoRegisterMallocSpy</b> does not directly call <b>AddRef</b> on <i>pMallocSpy</i>, but fully expects that the <b>QueryInterface</b> call will.



When the <a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a> object is registered, whenever there is a call to one of the <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> methods, OLE first calls the corresponding <b>IMallocSpy</b> pre-method. Then, after executing the <b>IMalloc</b> method, OLE calls the corresponding <b>IMallocSpy</b> post-method. For example, whenever there is a call to <a href="/windows/desktop/api/objidl/nf-objidl-imalloc-alloc">IMalloc::Alloc</a>, from whatever source, OLE calls <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-prealloc">IMallocSpy::PreAlloc</a>, calls <b>Alloc</b>, and after that allocation is completed, calls <a href="/windows/desktop/api/objidl/nf-objidl-imallocspy-postalloc">IMallocSpy::PostAlloc</a>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>



<a href="/windows/desktop/api/objbase/nf-objbase-corevokemallocspy">CoRevokeMallocSpy</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imallocspy">IMallocSpy</a>