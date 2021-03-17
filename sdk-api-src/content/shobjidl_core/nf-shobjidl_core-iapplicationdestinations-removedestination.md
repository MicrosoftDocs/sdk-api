---
UID: NF:shobjidl_core.IApplicationDestinations.RemoveDestination
title: IApplicationDestinations::RemoveDestination (shobjidl_core.h)
description: Removes a single destination from the Recent and Frequent categories in a Jump List.
helpviewer_keywords: ["IApplicationDestinations interface [Windows Shell]","RemoveDestination method","IApplicationDestinations.RemoveDestination","IApplicationDestinations::RemoveDestination","RemoveDestination","RemoveDestination method [Windows Shell]","RemoveDestination method [Windows Shell]","IApplicationDestinations interface","_shell_IApplicationDestinations_RemoveDestination","shell.IApplicationDestinations_RemoveDestination","shobjidl_core/IApplicationDestinations::RemoveDestination"]
old-location: shell\IApplicationDestinations_RemoveDestination.htm
tech.root: shell
ms.assetid: d1c33908-8450-4baf-8598-535a1941820c
ms.date: 12/05/2018
ms.keywords: IApplicationDestinations interface [Windows Shell],RemoveDestination method, IApplicationDestinations.RemoveDestination, IApplicationDestinations::RemoveDestination, RemoveDestination, RemoveDestination method [Windows Shell], RemoveDestination method [Windows Shell],IApplicationDestinations interface, _shell_IApplicationDestinations_RemoveDestination, shell.IApplicationDestinations_RemoveDestination, shobjidl_core/IApplicationDestinations::RemoveDestination
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDestinations::RemoveDestination
 - shobjidl_core/IApplicationDestinations::RemoveDestination
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
 - IApplicationDestinations.RemoveDestination
---

# IApplicationDestinations::RemoveDestination


## -description

Removes a single destination from the <b>Recent</b> and <b>Frequent</b> categories in a Jump List.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> that represents the destination to remove.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a standard COM error value otherwise. If the object pointed to by <i>punk</i> is not an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>, the method returns E_INVALIDARG.

## -remarks

A destination can appear in both the <b>Recent</b> and <b>Frequent</b> categories. If that is the case, this method removes the destination from both categories.

If the item is pinned to the list by the user, it is not removed but its usage data is cleared.

An application can call <b>RemoveDestination</b> without knowing if the item pointed to by <i>punk</i> is currently in the list. If there is no existing data on the item (in which case it is not in the <b>Recent</b> or <b>Frequent</b> list), this method does nothing and returns S_OK.

If the application has an explicit Application User Model ID (AppUserModelID), you must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid">IApplicationDestinations::SetAppID</a> before you call this method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations">IApplicationDestinations</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations">IApplicationDestinations::RemoveAllDestinations</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid">IApplicationDestinations::SetAppID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>