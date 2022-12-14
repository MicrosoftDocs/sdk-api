---
UID: NN:shobjidl_core.IEnumIDList
title: IEnumIDList (shobjidl_core.h)
description: Exposes a standard set of methods used to enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder.
helpviewer_keywords: ["IEnumIDList","IEnumIDList interface [Windows Shell]","IEnumIDList interface [Windows Shell]","described","_win32_IEnumIDList","shell.IEnumIDList","shobjidl_core/IEnumIDList"]
old-location: shell\IEnumIDList.htm
tech.root: shell
ms.assetid: b6f139d3-c54c-4350-9d8b-cd534909a488
ms.date: 12/05/2018
ms.keywords: IEnumIDList, IEnumIDList interface [Windows Shell], IEnumIDList interface [Windows Shell],described, _win32_IEnumIDList, shell.IEnumIDList, shobjidl_core/IEnumIDList
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumIDList
 - shobjidl_core/IEnumIDList
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
 - IEnumIDList
---

# IEnumIDList interface


## -description

Exposes a standard set of methods used to enumerate the pointers to item identifier lists (PIDLs) of the items in a Shell folder. When a folder's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> method is called, it creates an enumeration object and passes a pointer to the object's <b>IEnumIDList</b> interface back to the calling application.

## -inheritance

The <b>IEnumIDList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumIDList</b> also has these types of members:

## -remarks

All Shell folder objects must be able to respond to a call to their <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> method by creating an enumeration object that exports <b>IEnumIDList</b>. The Shell, in particular, uses these objects to enumerate the items in a folder.

Use this interface to enumerate the contents of a Shell folder object. Call the folder's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> method and use the returned <b>IEnumIDList</b> pointer to enumerate the PIDLs of the items in the folder.
