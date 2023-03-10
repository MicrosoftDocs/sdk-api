---
UID: NF:shobjidl_core.IFolderView2.SetGroupBy
title: IFolderView2::SetGroupBy (shobjidl_core.h)
description: Groups the view by the given property key and direction.
helpviewer_keywords: ["IFolderView2 interface [Windows Shell]","SetGroupBy method","IFolderView2.SetGroupBy","IFolderView2::SetGroupBy","SetGroupBy","SetGroupBy method [Windows Shell]","SetGroupBy method [Windows Shell]","IFolderView2 interface","_shell_IFolderView2_SetGroupBy","shell.IFolderView2_SetGroupBy","shobjidl_core/IFolderView2::SetGroupBy"]
old-location: shell\IFolderView2_SetGroupBy.htm
tech.root: shell
ms.assetid: 2d0761cb-7c81-48f7-994d-6dd61062d848
ms.date: 12/05/2018
ms.keywords: IFolderView2 interface [Windows Shell],SetGroupBy method, IFolderView2.SetGroupBy, IFolderView2::SetGroupBy, SetGroupBy, SetGroupBy method [Windows Shell], SetGroupBy method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetGroupBy, shell.IFolderView2_SetGroupBy, shobjidl_core/IFolderView2::SetGroupBy
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
 - IFolderView2::SetGroupBy
 - shobjidl_core/IFolderView2::SetGroupBy
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
 - IFolderView2.SetGroupBy
---

# IFolderView2::SetGroupBy


## -description

Groups the view by the given property key and direction.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> by which the view should be grouped.

### -param fAscending [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> to indicate sort order of the groups.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.