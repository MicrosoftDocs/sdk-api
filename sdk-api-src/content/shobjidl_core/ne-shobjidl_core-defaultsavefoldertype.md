---
UID: NE:shobjidl_core.DEFAULTSAVEFOLDERTYPE
title: DEFAULTSAVEFOLDERTYPE (shobjidl_core.h)
description: Specifies the default save location.
helpviewer_keywords: ["DEFAULTSAVEFOLDERTYPE","DEFAULTSAVEFOLDERTYPE enumeration [Windows Shell]","DSFT_DETECT","DSFT_PRIVATE","DSFT_PUBLIC","_shell_DEFAULTSAVEFOLDERTYPE","shell.DEFAULTSAVEFOLDERTYPE","shobjidl_core/DEFAULTSAVEFOLDERTYPE","shobjidl_core/DSFT_DETECT","shobjidl_core/DSFT_PRIVATE","shobjidl_core/DSFT_PUBLIC"]
old-location: shell\DEFAULTSAVEFOLDERTYPE.htm
tech.root: shell
ms.assetid: 51478854-03b2-4e1a-bc07-b9ca7e6cc33d
ms.date: 12/05/2018
ms.keywords: DEFAULTSAVEFOLDERTYPE, DEFAULTSAVEFOLDERTYPE enumeration [Windows Shell], DSFT_DETECT, DSFT_PRIVATE, DSFT_PUBLIC, _shell_DEFAULTSAVEFOLDERTYPE, shell.DEFAULTSAVEFOLDERTYPE, shobjidl_core/DEFAULTSAVEFOLDERTYPE, shobjidl_core/DSFT_DETECT, shobjidl_core/DSFT_PRIVATE, shobjidl_core/DSFT_PUBLIC
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DEFAULTSAVEFOLDERTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DEFAULTSAVEFOLDERTYPE
 - shobjidl_core/DEFAULTSAVEFOLDERTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - DEFAULTSAVEFOLDERTYPE
---

# DEFAULTSAVEFOLDERTYPE enumeration


## -description

Specifies the default save location.

## -enum-fields

### -field DSFT_DETECT:1

The current user determines the save folder. If the current user is the library's owner,  use the private save location (<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DSFT_PRIVATE</a>). If the current user is not the library's owner, use the public save location (<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype">DSFT_PUBLIC</a>).

### -field DSFT_PRIVATE

The library's private save location, which can only be accessed by the library's owner.

### -field DSFT_PUBLIC

The library's public save location, which can be accessed by all users.

## -remarks

These values cannot be combined.

<h3><a id="Used_By"></a><a id="used_by"></a><a id="USED_BY"></a>Used By</h3>
<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder">IShellLibrary::GetDefaultSaveFolder</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-setdefaultsavefolder">IShellLibrary::SetDefaultSaveFolder</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>
