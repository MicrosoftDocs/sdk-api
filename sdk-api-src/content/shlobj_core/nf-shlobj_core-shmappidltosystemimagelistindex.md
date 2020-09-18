---
UID: NF:shlobj_core.SHMapPIDLToSystemImageListIndex
title: SHMapPIDLToSystemImageListIndex function (shlobj_core.h)
description: SHMapPIDLToSystemImageListIndex may be altered or unavailable.
helpviewer_keywords: ["SHMapPIDLToSystemImageListIndex","SHMapPIDLToSystemImageListIndex function [Windows Shell]","_win32_SHMapPIDLToSystemImageListIndex","shell.SHMapPIDLToSystemImageListIndex","shlobj_core/SHMapPIDLToSystemImageListIndex"]
old-location: shell\SHMapPIDLToSystemImageListIndex.htm
tech.root: shell
ms.assetid: 7f11049b-2481-496b-95e3-77d480f2c9df
ms.date: 12/05/2018
ms.keywords: SHMapPIDLToSystemImageListIndex, SHMapPIDLToSystemImageListIndex function [Windows Shell], _win32_SHMapPIDLToSystemImageListIndex, shell.SHMapPIDLToSystemImageListIndex, shlobj_core/SHMapPIDLToSystemImageListIndex
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHMapPIDLToSystemImageListIndex
 - shlobj_core/SHMapPIDLToSystemImageListIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHMapPIDLToSystemImageListIndex
---

# SHMapPIDLToSystemImageListIndex function


## -description

<p class="CCE_Message">[<b>SHMapPIDLToSystemImageListIndex</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the icon index from the system image list that is associated with a folder item.

## -parameters

### -param pshf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

An <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface pointer for the folder that contains the item.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the item's <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

### -param piIndexSel [out, optional]

Type: <b>int*</b>

A pointer to an <b>int</b> that, when this function returns successfully, receives the index of the item's <b>open</b> icon in the system image list. If the item does not have a special <b>open</b> icon then the index of its normal icon is returned. If the <b>open</b> icon exists and cannot be obtained, then the value pointed to by <i>piIndex</i> is set to -1. This parameter can be <b>NULL</b> if the calling application is not interested in the <b>open</b> icon.

## -returns

Type: <b>int</b>

Returns the index of the item's normal icon in the system image list if successful, or -1 otherwise.