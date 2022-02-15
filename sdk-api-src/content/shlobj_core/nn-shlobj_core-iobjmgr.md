---
UID: NN:shlobj_core.IObjMgr
title: IObjMgr (shlobj_core.h)
description: Exposes methods that allow a client to append or remove an object from a collection of objects managed by a server object.
helpviewer_keywords: ["IObjMgr","IObjMgr interface [Windows Shell]","IObjMgr interface [Windows Shell]","described","_win32_IObjMgr","shell.IObjMgr","shlobj_core/IObjMgr"]
old-location: shell\IObjMgr.htm
tech.root: shell
ms.assetid: c0556a87-2be5-43dc-9ca6-dfbdae7e7137
ms.date: 12/05/2018
ms.keywords: IObjMgr, IObjMgr interface [Windows Shell], IObjMgr interface [Windows Shell],described, _win32_IObjMgr, shell.IObjMgr, shlobj_core/IObjMgr
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjMgr
 - shlobj_core/IObjMgr
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
 - IObjMgr
---

# IObjMgr interface


## -description

Exposes methods that allow a client to append or remove an object from a collection of objects managed by a server object.

## -inheritance

The <b>IObjMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjMgr</b> also has these types of members:

## -remarks

This interface is implemented by objects that manage a collection of other objects. It is exported to allow clients of the object to request that objects be added to or removed from the collection.

Use this interface to add or delete an object from the server object's collection of managed objects.
