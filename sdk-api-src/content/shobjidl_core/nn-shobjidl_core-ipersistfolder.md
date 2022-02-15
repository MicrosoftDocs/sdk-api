---
UID: NN:shobjidl_core.IPersistFolder
title: IPersistFolder (shobjidl_core.h)
description: Exposes a method that initializes Shell folder objects.
helpviewer_keywords: ["IPersistFolder","IPersistFolder interface [Windows Shell]","IPersistFolder interface [Windows Shell]","described","_win32_IPersistFolder","_win32_IPersistFolder_cpp","shell.IPersistFolder","shobjidl_core/IPersistFolder"]
old-location: shell\IPersistFolder.htm
tech.root: shell
ms.assetid: d37d4ca5-93a0-4090-b657-9b23d5df875c
ms.date: 12/05/2018
ms.keywords: IPersistFolder, IPersistFolder interface [Windows Shell], IPersistFolder interface [Windows Shell],described, _win32_IPersistFolder, _win32_IPersistFolder_cpp, shell.IPersistFolder, shobjidl_core/IPersistFolder
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
 - IPersistFolder
 - shobjidl_core/IPersistFolder
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
 - IPersistFolder
---

# IPersistFolder interface


## -description

Exposes a method that initializes Shell folder objects.

## -inheritance

The <b>IPersistFolder</b> interface inherits from <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>. <b>IPersistFolder</b> also has these types of members:

## -remarks

When you implement a Shell namespace extension, specifically the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface, you must implement this interface so the folder object can be initialized. Implementation of this interface is how the folder is told where it is in the Shell namespace.

You do not use this interface directly. It is used by the file system implementation of the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject">IShellFolder::BindToObject</a> interface when it is initializing a Shell folder object.
