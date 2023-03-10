---
UID: NN:shobjidl_core.IShellIcon
title: IShellIcon (shobjidl_core.h)
description: Exposes a method that obtains an icon index for an IShellFolder object.
helpviewer_keywords: ["IShellIcon","IShellIcon interface [Windows Shell]","IShellIcon interface [Windows Shell]","described","_win32_IShellIcon","shell.IShellIcon","shobjidl_core/IShellIcon"]
old-location: shell\IShellIcon.htm
tech.root: shell
ms.assetid: 64711453-bc70-4acb-bff7-8b5534cceff5
ms.date: 12/05/2018
ms.keywords: IShellIcon, IShellIcon interface [Windows Shell], IShellIcon interface [Windows Shell],described, _win32_IShellIcon, shell.IShellIcon, shobjidl_core/IShellIcon
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
 - IShellIcon
 - shobjidl_core/IShellIcon
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
 - IShellIcon
---

# IShellIcon interface


## -description

Exposes a method that obtains an icon index for an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object.

## -inheritance

The <b>IShellIcon</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellIcon</b> also has these types of members:

## -remarks

Implement <b>IShellIcon</b> when creating an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementation to provide a quick way to obtain the icon for an object in the folder.
      

If <b>IShellIcon</b> is not implemented by an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a> is used to retrieve an icon for all objects.
      

Use <b>IShellIcon</b> when retrieving the icon index for an item in a Shell folder.
      

<b>IShellIcon</b> allows an application to obtain the icon for any object within a folder by using only one instance of the interface. <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a>, on the other hand, requires that a separate instance of the interface be created for each object.
