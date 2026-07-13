---
UID: NS:shlobj_core.SHARDAPPIDINFOIDLIST
title: SHARDAPPIDINFOIDLIST (shlobj_core.h)
description: Contains data used by SHAddToRecentDocs to identify both an item — in this case by an absolute pointer to an item identifier list (PIDL) — and the process that it is associated with.
helpviewer_keywords: ["SHARDAPPIDINFOIDLIST","SHARDAPPIDINFOIDLIST structure [Windows Shell]","_shell_SHARDAPPIDINFOIDLIST","shell.SHARDAPPIDINFOIDLIST","shlobj_core/SHARDAPPIDINFOIDLIST"]
old-location: shell\SHARDAPPIDINFOIDLIST.htm
tech.root: shell
ms.assetid: 11c69ff9-b8a0-4168-8036-f45a9f7813ba
ms.date: 12/05/2018
ms.keywords: SHARDAPPIDINFOIDLIST, SHARDAPPIDINFOIDLIST structure [Windows Shell], _shell_SHARDAPPIDINFOIDLIST, shell.SHARDAPPIDINFOIDLIST, shlobj_core/SHARDAPPIDINFOIDLIST
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
req.typenames: SHARDAPPIDINFOIDLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHARDAPPIDINFOIDLIST
 - shlobj_core/SHARDAPPIDINFOIDLIST
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
 - SHARDAPPIDINFOIDLIST
---

# SHARDAPPIDINFOIDLIST structure


## -description

Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> to identify both an item—in this case by an absolute pointer to an item identifier list (PIDL)—and the process that it is associated with.

## -struct-fields

### -field pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

An absolute PIDL that gives the full path of the item in the Shell namespace.

### -field pszAppID

Type: <b>PCWSTR</b>

The application-defined AppUserModelID associated with the item.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo">SHARDAPPIDINFO</a>



<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink">SHARDAPPIDINFOLINK</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a>
