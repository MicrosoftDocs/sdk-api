---
UID: NF:ole2.OleSetContainedObject
title: OleSetContainedObject function (ole2.h)
description: Notifies an object that it is embedded in an OLE container, which ensures that reference counting is done correctly for containers that support links to embedded objects. (OleSetContainedObject)
helpviewer_keywords: ["OleSetContainedObject","OleSetContainedObject function [COM]","_ole_OleSetContainedObject","com.olesetcontainedobject","ole2/OleSetContainedObject"]
old-location: com\olesetcontainedobject.htm
tech.root: com
ms.assetid: 154aa6f0-3c02-4139-8c8e-c2112b015fe0
ms.date: 12/05/2018
ms.keywords: OleSetContainedObject, OleSetContainedObject function [COM], _ole_OleSetContainedObject, com.olesetcontainedobject, ole2/OleSetContainedObject
req.header: ole2.h
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
 - OleSetContainedObject
 - ole2/OleSetContainedObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleSetContainedObject
req.apiset: ext-ms-win-com-ole32-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# OleSetContainedObject function


## -description

Notifies an object that it is embedded in an OLE container, which ensures that reference counting is done correctly for containers that support links to embedded objects.

## -parameters

### -param pUnknown [in]

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the object.

### -param fContained [in]

<b>TRUE</b> if the object is an embedded object; <b>FALSE</b> otherwise.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>

## -remarks

The <b>OleSetContainedObject</b> function notifies an object that it is embedded in an OLE container. The implementation of <b>OleSetContainedObject</b> was changed in OLE 2.01 to coincide with the publication of the <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a> interface. You can use <b>OleSetContainedObject</b> and the <a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-setcontainedobject">IRunnableObject::SetContainedObject</a> method interchangeably. The <b>OleSetContainedObject</b> function queries the object for a pointer to the <b>IRunnableObject</b> interface. If successful, the function returns the results of calling <b>IRunnableObject::SetContainedObject</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-setcontainedobject">IRunnableObject::SetContainedObject</a>
