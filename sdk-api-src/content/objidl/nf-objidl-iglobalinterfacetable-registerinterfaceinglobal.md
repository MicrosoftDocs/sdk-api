---
UID: NF:objidl.IGlobalInterfaceTable.RegisterInterfaceInGlobal
title: IGlobalInterfaceTable::RegisterInterfaceInGlobal (objidl.h)
description: Registers the specified interface on an object residing in one apartment of a process as a global interface, enabling other apartments access to that interface.
helpviewer_keywords: ["IGlobalInterfaceTable interface [COM]","RegisterInterfaceInGlobal method","IGlobalInterfaceTable.RegisterInterfaceInGlobal","IGlobalInterfaceTable::RegisterInterfaceInGlobal","RegisterInterfaceInGlobal","RegisterInterfaceInGlobal method [COM]","RegisterInterfaceInGlobal method [COM]","IGlobalInterfaceTable interface","_com_iglobalinterfacetable_registerinterfaceinglobal","com.iglobalinterfacetable_registerinterfaceinglobal","objidlbase/IGlobalInterfaceTable::RegisterInterfaceInGlobal"]
old-location: com\iglobalinterfacetable_registerinterfaceinglobal.htm
tech.root: com
ms.assetid: 5282b0b8-4eab-4114-8061-6d74db3756b7
ms.date: 12/05/2018
ms.keywords: IGlobalInterfaceTable interface [COM],RegisterInterfaceInGlobal method, IGlobalInterfaceTable.RegisterInterfaceInGlobal, IGlobalInterfaceTable::RegisterInterfaceInGlobal, RegisterInterfaceInGlobal, RegisterInterfaceInGlobal method [COM], RegisterInterfaceInGlobal method [COM],IGlobalInterfaceTable interface, _com_iglobalinterfacetable_registerinterfaceinglobal, com.iglobalinterfacetable_registerinterfaceinglobal, objidlbase/IGlobalInterfaceTable::RegisterInterfaceInGlobal
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGlobalInterfaceTable::RegisterInterfaceInGlobal
 - objidl/IGlobalInterfaceTable::RegisterInterfaceInGlobal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IGlobalInterfaceTable.RegisterInterfaceInGlobal
---

# IGlobalInterfaceTable::RegisterInterfaceInGlobal


## -description

Registers the specified interface on an object residing in one apartment of a process as a global interface, enabling other apartments access to that interface.

## -parameters

### -param pUnk [in]

An interface pointer of type <i>riid</i> on the object on which the interface to be registered as global is implemented.

### -param riid [in]

The IID of the interface to be registered as global.

### -param pdwCookie [out]

An identifier that can be used by another apartment to get access to a pointer to the interface being registered. The value of an invalid cookie is 0.

## -returns

This method can return the following values.

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
The method completed successfully.

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
</table>

## -remarks

Called in the apartment in which an object resides to register one of the object's interfaces as a global interface. This method supplies a pointer to a cookie that other apartments can use in a call to the <a href="/windows/desktop/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal">GetInterfaceFromGlobal</a> method to get a pointer to that interface.

The interface pointer may be a pointer to an in-process object, or it may be a pointer to a proxy for an object residing in another apartment, in another process, or on another computer.

The apartment that calls this method must remain alive until the corresponding call to <a href="/windows/desktop/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal">RevokeInterfaceFromGlobal</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iglobalinterfacetable">IGlobalInterfaceTable</a>