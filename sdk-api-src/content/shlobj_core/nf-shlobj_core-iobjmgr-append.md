---
UID: NF:shlobj_core.IObjMgr.Append
title: IObjMgr::Append (shlobj_core.h)
description: Appends an object to the collection of managed objects.
helpviewer_keywords: ["Append","Append method [Windows Shell]","Append method [Windows Shell]","IObjMgr interface","IObjMgr interface [Windows Shell]","Append method","IObjMgr.Append","IObjMgr::Append","_win32_IObjMgr_Append","shell.IObjMgr_Append","shlobj_core/IObjMgr::Append"]
old-location: shell\IObjMgr_Append.htm
tech.root: shell
ms.assetid: a616f6d1-c1dc-4c1f-acf7-915cb0f722d6
ms.date: 12/05/2018
ms.keywords: Append, Append method [Windows Shell], Append method [Windows Shell],IObjMgr interface, IObjMgr interface [Windows Shell],Append method, IObjMgr.Append, IObjMgr::Append, _win32_IObjMgr_Append, shell.IObjMgr_Append, shlobj_core/IObjMgr::Append
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
 - IObjMgr::Append
 - shlobj_core/IObjMgr::Append
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
 - IObjMgr.Append
---

# IObjMgr::Append


## -description

Appends an object to the collection of managed objects.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The address of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the object to be added to the list.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr">IObjMgr</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iobjmgr-remove">IObjMgr::Remove</a>