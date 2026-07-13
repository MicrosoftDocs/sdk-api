---
UID: NS:shlobj_core.SHARDAPPIDINFO
title: SHARDAPPIDINFO (shlobj_core.h)
description: Contains data used by SHAddToRecentDocs to identify both an item - in this case as an IShellItem — and the process that it is associated with.
helpviewer_keywords: ["SHARDAPPIDINFO","SHARDAPPIDINFO structure [Windows Shell]","_shell_SHARDAPPIDINFO","shell.SHARDAPPIDINFO","shlobj_core/SHARDAPPIDINFO"]
old-location: shell\SHARDAPPIDINFO.htm
tech.root: shell
ms.assetid: bb2b7e86-04ca-4dd0-944b-a95e8a0be1e0
ms.date: 12/05/2018
ms.keywords: SHARDAPPIDINFO, SHARDAPPIDINFO structure [Windows Shell], _shell_SHARDAPPIDINFO, shell.SHARDAPPIDINFO, shlobj_core/SHARDAPPIDINFO
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHARDAPPIDINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHARDAPPIDINFO
 - shlobj_core/SHARDAPPIDINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHARDAPPIDINFO
---

# SHARDAPPIDINFO structure


## -description

Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> to identify both an item—in this case as an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>—and the process that it is associated with.

## -struct-fields

### -field psi

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the object in the Shell namespace.

### -field pszAppID

Type: <b>PCWSTR</b>

The application-defined AppUserModelID associated with the item.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist">SHARDAPPIDINFOIDLIST</a>



<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink">SHARDAPPIDINFOLINK</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a>
