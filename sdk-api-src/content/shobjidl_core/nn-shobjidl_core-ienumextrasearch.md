---
UID: NN:shobjidl_core.IEnumExtraSearch
title: IEnumExtraSearch (shobjidl_core.h)
description: A standard OLE enumerator used by a client to determine the available search objects for a folder.
helpviewer_keywords: ["IEnumExtraSearch","IEnumExtraSearch interface [Windows Shell]","IEnumExtraSearch interface [Windows Shell]","described","_win32_IEnumExtraSearch","shell.IEnumExtraSearch","shobjidl_core/IEnumExtraSearch"]
old-location: shell\IEnumExtraSearch.htm
tech.root: shell
ms.assetid: 63b71cd2-483b-482f-b3f4-6d5c937e7708
ms.date: 12/05/2018
ms.keywords: IEnumExtraSearch, IEnumExtraSearch interface [Windows Shell], IEnumExtraSearch interface [Windows Shell],described, _win32_IEnumExtraSearch, shell.IEnumExtraSearch, shobjidl_core/IEnumExtraSearch
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumExtraSearch
 - shobjidl_core/IEnumExtraSearch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEnumExtraSearch
---

# IEnumExtraSearch interface


## -description

A standard OLE enumerator used by a client to determine the available search objects for a folder.

## -inheritance

The <b>IEnumExtraSearch</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumExtraSearch</b> also has these types of members:

## -remarks

Implement <b>IEnumExtraSearch</b> if your namespace extension supports one or more search objects.

You do not call this interface directly. An <b>IEnumExtraSearch</b> interface is requested by a client only after it has determined that the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> interface is exposed. Clients retrieve a pointer to this interface by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-enumsearches">IShellFolder2::EnumSearches</a>.

<b>IEnumExtraSearch</b> implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and the standard OLE enumeration methods.
