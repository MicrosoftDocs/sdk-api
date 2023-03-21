---
UID: NF:shlobj_core.ILNext
title: ILNext function (shlobj_core.h)
description: Retrieves the next SHITEMID structure in an ITEMIDLIST structure. (ILNext)
helpviewer_keywords: ["ILNext","ILNext function [Windows Shell]","ILNext(PCUIDLIST_RELATIVE)","_shell_ILNext_PCUIDLIST_RELATIVE","shell.ILNext_PCUIDLIST_RELATIVE","shlobj_core/ILNext"]
old-location: shell\ILNext_PCUIDLIST_RELATIVE.htm
tech.root: shell
ms.assetid: 9f9650b3-1f0c-413c-bc32-29dd81556ce0
ms.date: 12/05/2018
ms.keywords: ILNext, ILNext function [Windows Shell], ILNext(PCUIDLIST_RELATIVE), _shell_ILNext_PCUIDLIST_RELATIVE, shell.ILNext_PCUIDLIST_RELATIVE, shlobj_core/ILNext
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
 - ILNext
 - shlobj_core/ILNext
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
 - ILNext
---

# ILNext function


## -description

Retrieves the next <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure in an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant, unaligned, relative PIDL for which the next <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure is being retrieved.

## -returns

Type: <b>PCUIDLIST_RELATIVE</b>

When this function returns, contains one of three results: If <i>pidl</i> is valid and not the last <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> in the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>, then it contains a pointer to the next <b>ITEMIDLIST</b> structure. If the last <b>ITEMIDLIST</b> structure is passed, it contains <b>NULL</b>, which signals the end of the PIDL. For other values of <i>pidl</i>, the return value is meaningless.

## -remarks

For use where STRICT_TYPED_ITEMIDS is defined.

To verify if the return value is <b>NULL</b>, use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty">ILIsEmpty</a>.
