---
UID: NF:shobjidl_core.IPersistFolder.Initialize
title: IPersistFolder::Initialize (shobjidl_core.h)
description: Instructs a Shell folder object to initialize itself based on the information passed.
helpviewer_keywords: ["IPersistFolder interface [Windows Shell]","Initialize method","IPersistFolder.Initialize","IPersistFolder::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IPersistFolder interface","_win32_IPersistFolder_Initialize","shell.IPersistFolder_Initialize","shobjidl_core/IPersistFolder::Initialize"]
old-location: shell\IPersistFolder_Initialize.htm
tech.root: shell
ms.assetid: 179f13c9-7306-4ed5-935e-2620616b46c1
ms.date: 12/05/2018
ms.keywords: IPersistFolder interface [Windows Shell],Initialize method, IPersistFolder.Initialize, IPersistFolder::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IPersistFolder interface, _win32_IPersistFolder_Initialize, shell.IPersistFolder_Initialize, shobjidl_core/IPersistFolder::Initialize
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
 - IPersistFolder::Initialize
 - shobjidl_core/IPersistFolder::Initialize
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
 - IPersistFolder.Initialize
---

# IPersistFolder::Initialize


## -description

Instructs a Shell folder object to initialize itself based on the information passed.

## -parameters

### -param pidl

Type: <b>LPCITEMIDLIST</b>

The address of the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> (item identifier list) structure that specifies the absolute location of the folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

All objects that implement the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface for use in the Shell's namespace must implement this method. When a folder's location in the namespace is not a relevant consideration, this method can simply return S_OK. When the location is relevant to the folder, you should store the fully qualified IDLIST passed in for later reference.

For example, if the folder implementation needs to construct a fully qualified pointer to an item identifier list (PIDL) to elements that it contains, the PIDL passed to this method should be used to construct the fully qualified PIDLs.