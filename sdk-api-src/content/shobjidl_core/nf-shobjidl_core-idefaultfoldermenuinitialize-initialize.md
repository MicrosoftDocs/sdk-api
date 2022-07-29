---
UID: NF:shobjidl_core.IDefaultFolderMenuInitialize.Initialize
title: IDefaultFolderMenuInitialize::Initialize (shobjidl_core.h)
description: . (IDefaultFolderMenuInitialize.Initialize)
helpviewer_keywords: ["IDefaultFolderMenuInitialize interface [Windows Shell]","Initialize method","IDefaultFolderMenuInitialize.Initialize","IDefaultFolderMenuInitialize::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IDefaultFolderMenuInitialize interface","shell.IDefaultFolderMenuInitialize_Initialize","shobjidl_core/IDefaultFolderMenuInitialize::Initialize"]
old-location: shell\IDefaultFolderMenuInitialize_Initialize.htm
tech.root: shell
ms.assetid: D837712B-1FF3-4021-BA50-E433BF5B24C2
ms.date: 12/05/2018
ms.keywords: IDefaultFolderMenuInitialize interface [Windows Shell],Initialize method, IDefaultFolderMenuInitialize.Initialize, IDefaultFolderMenuInitialize::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IDefaultFolderMenuInitialize interface, shell.IDefaultFolderMenuInitialize_Initialize, shobjidl_core/IDefaultFolderMenuInitialize::Initialize
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IDefaultFolderMenuInitialize::Initialize
 - shobjidl_core/IDefaultFolderMenuInitialize::Initialize
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
 - IDefaultFolderMenuInitialize.Initialize
---

# IDefaultFolderMenuInitialize::Initialize


## -description

Sets context menu info for the [IDefaultFolderMenuInitialize](nn-shobjidl_core-idefaultfoldermenuinitialize.md) object.

## -parameters

### -param hwnd [in]

A handle to the shortcut menu.

### -param pcmcb [in, optional]

Type: <b><a href="nn-shobjidl_core-icontextmenucb.md">IContextMenuCB</a>*</b>

The address of the object that defines the callback for the shortcut menu.

### -param pidlFolder [in, optional]

Type: **PCIDLIST_ABSOLUTE**

The address of an item identifier list that specifies the folder of the items. If NULL, this is computed from the *psf* parameter.

### -param psf [in, optional]

Type: <b><a href="nn-shobjidl_core-ishellfolder.md">IShellFolder</a>*</b>

The folder of the items.

### -param cidl [in]

Type: <b>UINT</b>

The count of items in the *apidl* parameter.

### -param apidl [in]

Type: <b>PCUITEMID_CHILD_ARRAY</b>

A pointer to an array of PIDL structures, each of which is an item to be operated on.

### -param punkAssociation [in, optional]

Type: <b>IUnknown*</b>

The address of an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> object that specifies where to load extensions from.

### -param cKeys [in]

Type: <b>UINT</b>

The count of items in the *aKeys* parameter. May be zero.

### -param aKeys [in, optional]

Type: <b>const HKEY*</b>

Specifies where to load extensions from.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize">IDefaultFolderMenuInitialize</a>
