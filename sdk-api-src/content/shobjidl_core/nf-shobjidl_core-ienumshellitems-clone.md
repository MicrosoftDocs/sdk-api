---
UID: NF:shobjidl_core.IEnumShellItems.Clone
title: IEnumShellItems::Clone (shobjidl_core.h)
description: Gets a copy of the current enumeration.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","IEnumShellItems interface","IEnumShellItems interface [Windows Shell]","Clone method","IEnumShellItems.Clone","IEnumShellItems::Clone","_shell_IEnumShellItems_Clone","shell.IEnumShellItems_Clone","shobjidl_core/IEnumShellItems::Clone"]
old-location: shell\IEnumShellItems_Clone.htm
tech.root: shell
ms.assetid: ccfe8ab0-8bc5-4270-9189-01bac38ce36a
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumShellItems interface, IEnumShellItems interface [Windows Shell],Clone method, IEnumShellItems.Clone, IEnumShellItems::Clone, _shell_IEnumShellItems_Clone, shell.IEnumShellItems_Clone, shobjidl_core/IEnumShellItems::Clone
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
 - IEnumShellItems::Clone
 - shobjidl_core/IEnumShellItems::Clone
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
 - IEnumShellItems.Clone
---

# IEnumShellItems::Clone


## -description

Gets a copy of the current enumeration.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a>**</b>

The address of a pointer that receives a copy of this enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>