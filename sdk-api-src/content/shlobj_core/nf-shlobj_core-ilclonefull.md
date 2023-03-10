---
UID: NF:shlobj_core.ILCloneFull
title: ILCloneFull function (shlobj_core.h)
description: Clones a full, or absolute, ITEMIDLIST structure.
helpviewer_keywords: ["ILCloneFull","ILCloneFull function [Windows Shell]","_shell_ILCloneFull","shell.ILCloneFull","shlobj_core/ILCloneFull"]
old-location: shell\ILCloneFull.htm
tech.root: shell
ms.assetid: 60af0eb7-306a-45f8-b5ce-eb6451f380d5
ms.date: 12/05/2018
ms.keywords: ILCloneFull, ILCloneFull function [Windows Shell], _shell_ILCloneFull, shell.ILCloneFull, shlobj_core/ILCloneFull
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILCloneFull
 - shlobj_core/ILCloneFull
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
 - ILCloneFull
---

# ILCloneFull function


## -description

Clones a full, or absolute, <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_ABSOLUTE</b>

A pointer to the full, or absolute, <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to be cloned.

## -returns

Type: <b>PIDLIST_ABSOLUTE</b>

A pointer to a copy of the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure pointed to by <i>pidl</i>.

## -remarks

When you are finished with the cloned <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure, release it with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> to avoid memory leaks.