---
UID: NS:shlobj._SFV_SETITEMPOS
title: SFV_SETITEMPOS (shlobj.h)
description: Stores position information for an item. Used with message SFVM_SETITEMPOS.
helpviewer_keywords: ["*LPSFV_SETITEMPOS","SFV_SETITEMPOS","SFV_SETITEMPOS structure [Windows Shell]","_shell_SFV_SETITEMPOS","shell.SFV_SETITEMPOS","shlobj/SFV_SETITEMPOS"]
old-location: shell\SFV_SETITEMPOS.htm
tech.root: shell
ms.assetid: 5ee6ef2b-2d06-42ec-b70e-659c2f137714
ms.date: 12/05/2018
ms.keywords: '*LPSFV_SETITEMPOS, SFV_SETITEMPOS, SFV_SETITEMPOS structure [Windows Shell], _shell_SFV_SETITEMPOS, shell.SFV_SETITEMPOS, shlobj/SFV_SETITEMPOS'
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SFV_SETITEMPOS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SFV_SETITEMPOS
 - shlobj/_SFV_SETITEMPOS
 - SFV_SETITEMPOS
 - shlobj/SFV_SETITEMPOS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - SFV_SETITEMPOS
---

# SFV_SETITEMPOS structure


## -description

Stores position information for an item. Used with message <a href="/windows/desktop/shell/sfvm-setitempos">SFVM_SETITEMPOS</a>.

## -struct-fields

### -field pidl

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> for the item.

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure indicating the position of the item.