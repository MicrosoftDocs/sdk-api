---
UID: NF:shlobj_core.ILCloneChild
title: ILCloneChild function (shlobj_core.h)
description: Clones a child ITEMIDLIST structure.
helpviewer_keywords: ["ILCloneChild","ILCloneChild function [Windows Shell]","_shell_ILCloneChild","shell.ILCloneChild","shlobj_core/ILCloneChild"]
old-location: shell\ILCloneChild.htm
tech.root: shell
ms.assetid: e82f0b34-3d7d-4da2-9eec-05842ede8300
ms.date: 12/05/2018
ms.keywords: ILCloneChild, ILCloneChild function [Windows Shell], _shell_ILCloneChild, shell.ILCloneChild, shlobj_core/ILCloneChild
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
 - ILCloneChild
 - shlobj_core/ILCloneChild
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
 - ILCloneChild
---

# ILCloneChild function


## -description

Clones a child <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the child <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure to be cloned.

## -returns

Type: <b>PCUITEMID_CHILD</b>

A pointer to a copy of the child <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure pointed to by <i>pidl</i>.

## -remarks

When you are finished with the cloned <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure, release it with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a> to avoid memory leaks.