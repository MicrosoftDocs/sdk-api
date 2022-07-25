---
UID: NN:shlobj_core.IQueryInfo
title: IQueryInfo (shlobj_core.h)
description: Exposes methods that the Shell uses to retrieve flags and info tip information for an item that resides in an IShellFolder implementation. Info tips are usually displayed inside a tooltip control.
helpviewer_keywords: ["IQueryInfo","IQueryInfo interface [Windows Shell]","IQueryInfo interface [Windows Shell]","described","_win32_IQueryInfo","shell.IQueryInfo","shlobj_core/IQueryInfo"]
old-location: shell\IQueryInfo.htm
tech.root: shell
ms.assetid: 7e256ed3-b3c7-4f9d-b3a0-e33c46fa2573
ms.date: 12/05/2018
ms.keywords: IQueryInfo, IQueryInfo interface [Windows Shell], IQueryInfo interface [Windows Shell],described, _win32_IQueryInfo, shell.IQueryInfo, shlobj_core/IQueryInfo
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryInfo
 - shlobj_core/IQueryInfo
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
 - IQueryInfo
---

# IQueryInfo interface


## -description

Exposes methods that the Shell uses to retrieve flags and info tip information for an item that resides in an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementation. Info tips are usually displayed inside a <a href="/previous-versions/windows/desktop/legacy/hh449606(v=vs.85)">tooltip</a> control.

## -inheritance

The <b>IQueryInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryInfo</b> also has these types of members:

## -remarks

This interface is obtained by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> and passing IID_IQueryInfo for the interface identifier. The item for which info tip information is being requested is contained in the <i>apidl</i> argument of the <b>IShellFolder::GetUIObjectOf</b> call. If <b>IQueryInfo</b> is not supplied by the folder, the Shell will use the standard display text in the info tip.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IQueryInfo</b> to provide flags and text information that differs from the normal text that is displayed for an item in a folder. For example, if your folder contained file objects, you could use the info tip to provide the entire path and file name for the item rather than just the file name.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
In most cases, you do not use this interface directly. The Shell will use this interface when it requires additional information to display inside of an info tip. However, you can use <b>IQueryInfo</b> directly if you want to obtain info tip information from another object.
