---
UID: NF:shobjidl_core.IDefaultFolderMenuInitialize.SetHandlerClsid
title: IDefaultFolderMenuInitialize::SetHandlerClsid (shobjidl_core.h)
description: . (IDefaultFolderMenuInitialize.SetHandlerClsid)
helpviewer_keywords: ["IDefaultFolderMenuInitialize interface [Windows Shell]","SetHandlerClsid method","IDefaultFolderMenuInitialize.SetHandlerClsid","IDefaultFolderMenuInitialize::SetHandlerClsid","SetHandlerClsid","SetHandlerClsid method [Windows Shell]","SetHandlerClsid method [Windows Shell]","IDefaultFolderMenuInitialize interface","shell.IDefaultFolderMenuInitialize_SetHandlerClsid","shobjidl_core/IDefaultFolderMenuInitialize::SetHandlerClsid"]
old-location: shell\IDefaultFolderMenuInitialize_SetHandlerClsid.htm
tech.root: shell
ms.assetid: 90D861DA-33B7-4054-888E-86B504B2C5D1
ms.date: 12/05/2018
ms.keywords: IDefaultFolderMenuInitialize interface [Windows Shell],SetHandlerClsid method, IDefaultFolderMenuInitialize.SetHandlerClsid, IDefaultFolderMenuInitialize::SetHandlerClsid, SetHandlerClsid, SetHandlerClsid method [Windows Shell], SetHandlerClsid method [Windows Shell],IDefaultFolderMenuInitialize interface, shell.IDefaultFolderMenuInitialize_SetHandlerClsid, shobjidl_core/IDefaultFolderMenuInitialize::SetHandlerClsid
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
 - IDefaultFolderMenuInitialize::SetHandlerClsid
 - shobjidl_core/IDefaultFolderMenuInitialize::SetHandlerClsid
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
 - IDefaultFolderMenuInitialize.SetHandlerClsid
---

# IDefaultFolderMenuInitialize::SetHandlerClsid


## -description

Sets the shortcut menu handler for the [IDefaultFolderMenuInitialize](nn-shobjidl_core-idefaultfoldermenuinitialize.md) object.

## -parameters

### -param rclsid [in]

Type: <b>REFCLSID</b>

The CLSID for the object defines the shortcut menu handler.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize">IDefaultFolderMenuInitialize</a>
