---
UID: NN:shobjidl_core.IDefaultFolderMenuInitialize
title: IDefaultFolderMenuInitialize (shobjidl_core.h)
description: Provides methods used to get and set shortcut menu information. This information is the same as that provided to SHCreateDefaultContextMenu through the DEFCONTEXTMENU structure.
helpviewer_keywords: ["IDefaultFolderMenuInitialize","IDefaultFolderMenuInitialize interface [Windows Shell]","IDefaultFolderMenuInitialize interface [Windows Shell]","described","shell.IDefaultFolderMenuInitialize","shobjidl_core/IDefaultFolderMenuInitialize"]
old-location: shell\IDefaultFolderMenuInitialize.htm
tech.root: shell
ms.assetid: 23C75435-E43D-4451-8F03-AE051BC1B66D
ms.date: 12/05/2018
ms.keywords: IDefaultFolderMenuInitialize, IDefaultFolderMenuInitialize interface [Windows Shell], IDefaultFolderMenuInitialize interface [Windows Shell],described, shell.IDefaultFolderMenuInitialize, shobjidl_core/IDefaultFolderMenuInitialize
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
 - IDefaultFolderMenuInitialize
 - shobjidl_core/IDefaultFolderMenuInitialize
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
 - IDefaultFolderMenuInitialize
---

# IDefaultFolderMenuInitialize interface


## -description

Provides methods used to get and set shortcut menu information. This information is the same as that provided to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu">SHCreateDefaultContextMenu</a> through the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu">DEFCONTEXTMENU</a> structure.
<div class="alert"><b>Note</b>  Do not use this method to reinitialize a shortcut menu; use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize">IShellExtInit::Initialize</a> instead.</div><div> </div>

## -inheritance

The <b>IDefaultFolderMenuInitialize</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDefaultFolderMenuInitialize</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
