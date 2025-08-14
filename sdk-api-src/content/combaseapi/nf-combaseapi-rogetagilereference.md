---
UID: NF:combaseapi.RoGetAgileReference
title: RoGetAgileReference function (combaseapi.h)
description: Creates an agile reference for an object specified by the given interface.
helpviewer_keywords: ["RoGetAgileReference","RoGetAgileReference function [Windows Runtime]","combaseapi/RoGetAgileReference","winrt.rogetagilereference"]
old-location: winrt\rogetagilereference.htm
tech.root: WinRT
ms.assetid: D16224C7-1BB7-46F5-B66C-54D0B9679006
ms.date: 12/05/2018
ms.keywords: RoGetAgileReference, RoGetAgileReference function [Windows Runtime], combaseapi/RoGetAgileReference, winrt.rogetagilereference
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - RoGetAgileReference
 - combaseapi/RoGetAgileReference
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
 - API-MS-Win-Core-Com-l1-1-1.dll
 - ComBase.dll
api_name:
 - RoGetAgileReference
---

# RoGetAgileReference function


## -description

Creates an agile reference for an object specified by the given interface.

## -parameters

### -param options [in]

The registration options.

### -param riid [in]

The interface ID of the object for which an agile reference is being obtained.

### -param pUnk [in]

Pointer to the interface to be encapsulated in an agile reference. It must be the same type as <i>riid</i>. It may be a pointer to an in-process object or a pointer to a proxy of an object.

### -param ppAgileReference [out]

The agile reference for the object. Call the <a href="/windows/desktop/WinRT/iagilereference-resolve">Resolve</a> method to localize the object into the apartment in which <b>Resolve</b> is called.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
The <i>options</i> parameter in invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_OUTOFMEMORY</dt>
</dl>
</td>
<td width="60%">
The agile reference couldn't be constructed due to an out-of-memory condition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_NOINTERFACE</dt>
</dl>
</td>
<td width="60%">
The <i>pUnk</i> parameter doesn't support the interface ID specified by the <i>riid</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CO_E_NOT_SUPPORTED</dt>
</dl>
</td>
<td width="60%">
The object implements the <a href="/windows/desktop/api/objidl/nn-objidl-inomarshal">INoMarshal</a> interface.

</td>
</tr>
</table>

## -remarks

Call the <b>RoGetAgileReference</b> function on an existing object to request an agile reference to the object. The object may or may not be agile, but the returned <a href="/windows/desktop/api/objidl/nn-objidl-iagilereference">IAgileReference</a> is agile. The agile reference can be passed to another apartment within the same process, where the original object is retrieved by using the <b>IAgileReference</b> interface.

This is conceptually similar to the existing Global Interface Table (GIT). Rather than interacting with the GIT, an <a href="/windows/desktop/api/objidl/nn-objidl-iagilereference">IAgileReference</a> is obtained and used to retrieve the object directly. Just as the GIT is per-process only, agile references are per-process and can't be marshaled.

The agile reference feature provides a performance improvement over the GIT. The agile reference performs eager marshaling by default, which saves a cross-apartment call in cases where the object is retrieved from the agile reference in an apartment that's different from where the agile reference was created. For additional performance improvement, users of the <b>RoGetAgileReference</b> function can use the same interface to create an <a href="/windows/desktop/api/objidl/nn-objidl-iagilereference">IAgileReference</a> and resolve the original object. This saves an additional <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> call to obtain the desired interface from the resolved object.

For example, you have a non-agile object named CDemoExample, which implements the IDemo and IExample interfaces. Call the <b>RoGetAgileReference</b> function and pass the object, with IID_IDemo. You get back an <a href="/windows/desktop/api/objidl/nn-objidl-iagilereference">IAgileReference</a> interface pointer, which is agile, so you can pass it to a different apartment. In the other apartment, call the <a href="/windows/desktop/WinRT/iagilereference-resolve">Resolve</a> method, with IID_IExample. You get back an IExample pointer that you can use within this apartment. This IExample pointer is an IExample proxy that's connected to the original CDemoExample object. The agile reference handles the complexity of operations like manually marshaling to a stream and unmarshaling on the other side of the apartment boundary.

## -see-also

<a href="/windows/desktop/api/combaseapi/ne-combaseapi-agilereferenceoptions">AgileReferenceOptions</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iagilereference">IAgileReference</a>
