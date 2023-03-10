---
UID: NF:objbase.CoGetObject
title: CoGetObject function (objbase.h)
description: Converts a display name into a moniker that identifies the object named, and then binds to the object identified by the moniker.
helpviewer_keywords: ["CoGetObject","CoGetObject function [COM]","_com_CoGetObject","com.cogetobject","objbase/CoGetObject"]
old-location: com\cogetobject.htm
tech.root: com
ms.assetid: 0f5c9ef5-3918-4f93-bfd1-1017029b3dc1
ms.date: 12/05/2018
ms.keywords: CoGetObject, CoGetObject function [COM], _com_CoGetObject, com.cogetobject, objbase/CoGetObject
req.header: objbase.h
req.include-header: 
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
 - CoGetObject
 - objbase/CoGetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-OLE32-bindctx-l1-1-0.dll
 - ole32_wp.dll
api_name:
 - CoGetObject
---

# CoGetObject function


## -description

Converts a display name into a moniker that identifies the object named, and then binds to the object identified by the moniker.

## -parameters

### -param pszName [in]

The display name of the object to be created.

### -param pBindOptions [in, optional]

The binding options used to create a moniker that creates the actual object. For details, see <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a>. This parameter can be <b>NULL</b>.

### -param riid [in]

A reference to the identifier of an interface that is implemented on the object to be created.

### -param ppv [out]

The address of a pointer to the interface specified by <i>riid</i> on the object that is created.

## -returns

This function can return the standard return values E_FAIL, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The object was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszName</i> parameter is not a properly formed display name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object identified by this moniker, or some object identified by the composite moniker of which this moniker is a part, could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_EXCEEDEDDEADLINE</b></dt>
</dl>
</td>
<td width="60%">
The binding operation could not be completed within the time limit specified by the <a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a> structure passed in <i>pBindOptions</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_CONNECTMANUALLY</b></dt>
</dl>
</td>
<td width="60%">
The binding operation requires assistance from the end user. The most common reasons for returning this value are that a password is needed or that a floppy needs to be mounted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_INTERMEDIATEINTERFACENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
An intermediate object was found but it did not support an interface required to complete the binding operation. For example, an item moniker returns this value if its container does not support the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interface.

</td>
</tr>
</table>

## -remarks

<b>CoGetObject</b> encapsulates calls to the COM library functions <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>, <a href="/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a>.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a>