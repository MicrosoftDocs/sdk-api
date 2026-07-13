---
UID: NF:shobjidl_core.IApplicationDestinations.RemoveAllDestinations
title: IApplicationDestinations::RemoveAllDestinations (shobjidl_core.h)
description: Clears all destination entries from the Recent and Frequent categories in an application's Jump List.
helpviewer_keywords: ["IApplicationDestinations interface [Windows Shell]","RemoveAllDestinations method","IApplicationDestinations.RemoveAllDestinations","IApplicationDestinations::RemoveAllDestinations","RemoveAllDestinations","RemoveAllDestinations method [Windows Shell]","RemoveAllDestinations method [Windows Shell]","IApplicationDestinations interface","_shell_IApplicationDestinations_RemoveAllDestinations","shell.IApplicationDestinations_RemoveAllDestinations","shobjidl_core/IApplicationDestinations::RemoveAllDestinations"]
old-location: shell\IApplicationDestinations_RemoveAllDestinations.htm
tech.root: shell
ms.assetid: bda83a9a-9759-47cc-8d15-ac55583a5810
ms.date: 12/05/2018
ms.keywords: IApplicationDestinations interface [Windows Shell],RemoveAllDestinations method, IApplicationDestinations.RemoveAllDestinations, IApplicationDestinations::RemoveAllDestinations, RemoveAllDestinations, RemoveAllDestinations method [Windows Shell], RemoveAllDestinations method [Windows Shell],IApplicationDestinations interface, _shell_IApplicationDestinations_RemoveAllDestinations, shell.IApplicationDestinations_RemoveAllDestinations, shobjidl_core/IApplicationDestinations::RemoveAllDestinations
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
 - IApplicationDestinations::RemoveAllDestinations
 - shobjidl_core/IApplicationDestinations::RemoveAllDestinations
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
 - IApplicationDestinations.RemoveAllDestinations
---

# IApplicationDestinations::RemoveAllDestinations


## -description

Clears all destination entries from the <b>Recent</b> and <b>Frequent</b> categories in an application's Jump List.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method does not remove items that the user has pinned to the Jump List. Those items cannot be removed programmatically; only the user can remove them. However, it does remove usage data for those pinned items. It also cannot remove items from custom categories or the task list.

If the application has an explicit Application User Model ID (AppUserModelID), you must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid">IApplicationDestinations::SetAppID</a> before you call this method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations">IApplicationDestinations</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination">IApplicationDestinations::RemoveDestination</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid">IApplicationDestinations::SetAppID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
