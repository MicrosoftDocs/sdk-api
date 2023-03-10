---
UID: NN:shobjidl_core.IColumnManager
title: IColumnManager (shobjidl_core.h)
description: Exposes methods that enable inspection and manipulation of columns in the Windows Explorer Details view. Each column is referenced by a PROPERTYKEY structure, which names a property.
helpviewer_keywords: ["IColumnManager","IColumnManager interface [Windows Shell]","IColumnManager interface [Windows Shell]","described","shell.IColumnManager","shell_IColumnManager","shobjidl_core/IColumnManager"]
old-location: shell\IColumnManager.htm
tech.root: shell
ms.assetid: d01cacd8-1867-4f44-bbc3-876bd727c0fe
ms.date: 12/05/2018
ms.keywords: IColumnManager, IColumnManager interface [Windows Shell], IColumnManager interface [Windows Shell],described, shell.IColumnManager, shell_IColumnManager, shobjidl_core/IColumnManager
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IColumnManager
 - shobjidl_core/IColumnManager
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
 - IColumnManager
---

# IColumnManager interface


## -description

Exposes methods that enable inspection and manipulation of columns in the Windows Explorer Details view. Each column is referenced by a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure, which names a property.

## -inheritance

The <b>IColumnManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IColumnManager</b> also has these types of members:

## -remarks

This interface can be accessed even when the Windows Explorer window is in a non-column view mode such as icons, thumbnails, or tiles. It affects those views, as well as views in which the column header control displays the set of columns to which <b>IColumnManager</b> provides access.

The default implementation of the Windows Explorer view object, created by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>, supports this interface retrieved through <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>. Code that runs in the Windows Explorer (such as view callbacks, context menus or drop targets) can access the view object using <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">IServiceProvider::QueryService</a>, querying for <b>SID_SFolderView</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2">IFolderView2</a>
