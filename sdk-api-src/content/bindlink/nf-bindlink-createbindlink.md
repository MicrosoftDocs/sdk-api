---
UID: NF:bindlink.CreateBindLink
tech.root: fs
title: CreateBindLink (bindlink.h)
ms.date: 05/01/2023
targetos: Windows
description: This API allows admins to create a bind link between a virtual path and a backing path.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: bindlink.dll
req.header: bindlink.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: bindlink.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - bindlink.h
api_name:
 - CreateBindLink
f1_keywords:
 - CreateBindLink
 - bindlink/CreateBindLink
dev_langs:
 - c++
helpviewer_keywords:
 - CreateBindLink
---

## -description

This API allows admins to create a bind link between a virtual path and a backing path. The virtual path is always local while the backing path could be local or remote (a network share, for example). The parent of the *virtualPath* should be visible for the link creation to succeed. Both the virtual path and the backing path can represent files or directories. The *backingPath* for a prior link can be a *virtualPath* for a subsequent link as well. **CreateBindLink** can only be called by a user with Administrator privileges. Once created, a bind link exists system-wide, and it lasts until it is deleted by calling [RemoveBindLink](nf-bindlink-removebindlink.md), or until the system is shut down.

## -parameters

### -param virtualPath

The virtual path to be used to create the bind link.

### -param backingPath

The backing path to be used to create the bind link.

### -param createBindLinkFlags

These flags can change the default bind link behavior to suit the needs of the user. See [CREATE_BIND_LINK_FLAGS](ne-bindlink-create_bind_link_flags.md) for more details.

### -param exceptionCount

The number of exceptions provided in the *exceptionPaths* parameter.

### -param exceptionPaths

The exception paths to be excluded from the bind link. Note that exceptions do not apply to anchorless links since anchorless virtual paths have no descendants by definition and, therefore, have no paths that qualify. The API will return an error if there is an attempt to pass exceptions to anchorless link.

## -returns

## -remarks

For more information about creating bind links, see [Bindlink Overview - Creating bind links](/windows/win32/bindlink/bindlink-overview#create-bind-links).

#### Examples

For a full example of how to use the **CreateBindLink** and **RemoveBindLink** APIs, see the [bind link example](/windows/win32/bindlink/bindlink-example) page.

## -see-also

[RemoveBindLink](nf-bindlink-removebindlink.md)
