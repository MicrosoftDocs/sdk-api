---
UID: NF:shlobj_core.ILIsAligned
title: ILIsAligned function (shlobj_core.h)
description: Verifies whether a constant ITEMIDLIST is aligned on a pointer boundary, which is a DWORD on 32-bit architectures and a QWORD on 64-bit architectures.
helpviewer_keywords: ["ILIsAligned","ILIsAligned function [Windows Shell]","_shell_ILIsAligned","shell.ILIsAligned","shlobj_core/ILIsAligned"]
old-location: shell\ILIsAligned.htm
tech.root: shell
ms.assetid: ef6607c6-3ea0-4b45-b443-dbd1359ab873
ms.date: 12/05/2018
ms.keywords: ILIsAligned, ILIsAligned function [Windows Shell], _shell_ILIsAligned, shell.ILIsAligned, shlobj_core/ILIsAligned
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
 - ILIsAligned
 - shlobj_core/ILIsAligned
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
 - ILIsAligned
---

# ILIsAligned function


## -description

Verifies whether a constant <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> is aligned on a pointer boundary, which is a <b>DWORD</b> on 32-bit architectures and a <b>QWORD</b> on 64-bit architectures.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant PIDL relative to a parent folder that is being checked for alignment.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if aligned; otherwise, <b>FALSE</b>.

## -remarks

For use where STRICT_TYPED_ITEMIDS is defined.