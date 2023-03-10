---
UID: NN:shobjidl_core.IPersistFolder3
title: IPersistFolder3 (shobjidl_core.h)
description: Extends the IPersistFolder and IPersistFolder2 interfaces by allowing a folder object to implement nondefault handling of folder shortcuts.
helpviewer_keywords: ["IPersistFolder3","IPersistFolder3 interface [Windows Shell]","IPersistFolder3 interface [Windows Shell]","described","_win32_IPersistFolder3","shell.IPersistFolder3","shobjidl_core/IPersistFolder3"]
old-location: shell\IPersistFolder3.htm
tech.root: shell
ms.assetid: 77a10997-1512-41ee-a84c-f3fa2e500d20
ms.date: 12/05/2018
ms.keywords: IPersistFolder3, IPersistFolder3 interface [Windows Shell], IPersistFolder3 interface [Windows Shell],described, _win32_IPersistFolder3, shell.IPersistFolder3, shobjidl_core/IPersistFolder3
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP3, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IPersistFolder3
 - shobjidl_core/IPersistFolder3
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
 - IPersistFolder3
---

# IPersistFolder3 interface


## -description

Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder">IPersistFolder</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2">IPersistFolder2</a> interfaces by allowing a folder object to implement nondefault handling of folder shortcuts.

## -inheritance

The <b>IPersistFolder3</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2">IPersistFolder2</a>. <b>IPersistFolder3</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder">IPersistFolder</a>, and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2">IPersistFolder2</a> interfaces, from which it inherits.

In Windows versions earlier than Windows Vista, this interface was declared in Shlobj.h.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Namespace extensions implement this interface if they need to perform nondefault handling of folder shortcuts.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications do not normally use this interface directly.
