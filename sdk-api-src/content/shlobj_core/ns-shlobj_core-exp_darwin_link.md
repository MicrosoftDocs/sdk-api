---
UID: NS:shlobj_core.EXP_DARWIN_LINK
title: EXP_DARWIN_LINK (shlobj_core.h)
description: Holds an extra data block used by IShellLinkDataList. It holds the link's Windows Installer ID.
helpviewer_keywords: ["*LPEXP_DARWIN_LINK","EXP_DARWIN_ID_SIG","EXP_DARWIN_LINK","EXP_DARWIN_LINK structure [Windows Shell]","LPEXP_DARWIN_LINK","LPEXP_DARWIN_LINK structure pointer [Windows Shell]","_win32_EXP_DARWIN_LINK_str","shell.EXP_DARWIN_LINK_str","shlobj_core/EXP_DARWIN_LINK","shlobj_core/LPEXP_DARWIN_LINK"]
old-location: shell\EXP_DARWIN_LINK_str.htm
tech.root: shell
ms.assetid: 016c539e-6035-4752-99b6-71e2d7199bf0
ms.date: 12/05/2018
ms.keywords: '*LPEXP_DARWIN_LINK, EXP_DARWIN_ID_SIG, EXP_DARWIN_LINK, EXP_DARWIN_LINK structure [Windows Shell], LPEXP_DARWIN_LINK, LPEXP_DARWIN_LINK structure pointer [Windows Shell], _win32_EXP_DARWIN_LINK_str, shell.EXP_DARWIN_LINK_str, shlobj_core/EXP_DARWIN_LINK, shlobj_core/LPEXP_DARWIN_LINK'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: EXP_DARWIN_LINK, *LPEXP_DARWIN_LINK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPEXP_DARWIN_LINK
 - shlobj_core/LPEXP_DARWIN_LINK
 - EXP_DARWIN_LINK
 - shlobj_core/EXP_DARWIN_LINK
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
 - EXP_DARWIN_LINK
---

# EXP_DARWIN_LINK structure


## -description

Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>. It holds the link's Windows Installer ID.

## -struct-fields

### -field dbh

Type: <b><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header">DATABLOCK_HEADER</a></b>


<a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header">DATABLOCK_HEADER</a> structure stating the size and signature of the <b>EXP_DARWIN_LINK</b> structure. The following is the only recognized signature value.



#### EXP_DARWIN_ID_SIG

The <b>EXP_DARWIN_LINK</b> structure contains a Windows Installer ID.

### -field DUMMYSTRUCTNAME

### -field szDarwinID

Type: <b>__wchar_t[MAX_PATH]</b>

The link's ID in the form of an ANSI string.

### -field szwDarwinID

Type: <b>WCHAR[MAX_PATH]</b>

The link's ID in the form of an Unicode string.

## -remarks

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags">IShellLinkDataList::GetFlags</a> returns the flag SLDF_HAS_DARWINID for links that have a darwin signature.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags">IShellLinkDataList::GetFlags</a>

