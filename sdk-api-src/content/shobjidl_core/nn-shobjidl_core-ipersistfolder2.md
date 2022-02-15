---
UID: NN:shobjidl_core.IPersistFolder2
title: IPersistFolder2 (shobjidl_core.h)
description: Exposes methods that obtain information from Shell folder objects.
helpviewer_keywords: ["IPersistFolder2","IPersistFolder2 interface [Windows Shell]","IPersistFolder2 interface [Windows Shell]","described","_win32_IPersistFolder2","shell.IPersistFolder2","shobjidl_core/IPersistFolder2"]
old-location: shell\IPersistFolder2.htm
tech.root: shell
ms.assetid: 3deb3467-b6f2-49f9-ba24-fd2cca80f247
ms.date: 12/05/2018
ms.keywords: IPersistFolder2, IPersistFolder2 interface [Windows Shell], IPersistFolder2 interface [Windows Shell],described, _win32_IPersistFolder2, shell.IPersistFolder2, shobjidl_core/IPersistFolder2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistFolder2
 - shobjidl_core/IPersistFolder2
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
 - IPersistFolder2
---

# IPersistFolder2 interface


## -description

Exposes methods that obtain information from Shell folder objects.

## -inheritance

The <b>IPersistFolder2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder">IPersistFolder</a>. <b>IPersistFolder2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder">IPersistFolder</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
When implementing a Shell namespace extension, specifically the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface, you need to implement this interface so that the Shell folder object's <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> can be retrieved.
