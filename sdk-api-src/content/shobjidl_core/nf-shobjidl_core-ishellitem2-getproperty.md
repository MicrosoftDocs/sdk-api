---
UID: NF:shobjidl_core.IShellItem2.GetProperty
title: IShellItem2::GetProperty (shobjidl_core.h)
description: Gets a PROPVARIANT structure from a specified property key.
helpviewer_keywords: ["GetProperty","GetProperty method [Windows Shell]","GetProperty method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetProperty method","IShellItem2.GetProperty","IShellItem2::GetProperty","_shell_IShellItem2_GetProperty","shell.IShellItem2_GetProperty","shobjidl_core/IShellItem2::GetProperty"]
old-location: shell\IShellItem2_GetProperty.htm
tech.root: shell
ms.assetid: f72e23b9-e99b-462b-91b6-9ef27a4fc9e1
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Shell], GetProperty method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetProperty method, IShellItem2.GetProperty, IShellItem2::GetProperty, _shell_IShellItem2_GetProperty, shell.IShellItem2_GetProperty, shobjidl_core/IShellItem2::GetProperty
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IShellItem2::GetProperty
 - shobjidl_core/IShellItem2::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItem2.GetProperty
---

# IShellItem2::GetProperty


## -description

Gets a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure from a specified property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Contains a pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.