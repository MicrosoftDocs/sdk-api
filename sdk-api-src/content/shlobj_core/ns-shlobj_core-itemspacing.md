---
UID: NS:shlobj_core._ITEMSPACING
title: ITEMSPACING (shlobj_core.h)
description: Stores the dimensions of the two possible sizes of icon spacing that are available for display:\_small and large. Used by IShellFolderView::GetItemSpacing.
old-location: shell\ITEMSPACING.htm
tech.root: shell
ms.assetid: fcd7f3da-6aba-4683-bd5e-14a6b5f93cb5
ms.date: 12/05/2018
ms.keywords: ITEMSPACING, ITEMSPACING structure [Windows Shell], _ITEMSPACING, _shell_ITEMSPACING, shell.ITEMSPACING, shlobj_core/ITEMSPACING
f1_keywords:
- shlobj_core/ITEMSPACING
dev_langs:
- c++
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- shlobj_core.h
api_name:
- ITEMSPACING
targetos: Windows
req.typenames: ITEMSPACING
req.redist: 
ms.custom: 19H1
---

# ITEMSPACING structure


## -description


Stores the dimensions of the two possible sizes of icon spacing that are available for display: small and large. Used by <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing">IShellFolderView::GetItemSpacing</a>.


## -struct-fields




### -field cxSmall

Type: <b>int</b>

The width of the spacing between icons in small icon mode, in pixels.


### -field cySmall

Type: <b>int</b>

The height of the spacing between icons in small icon mode, in pixels.


### -field cxLarge

Type: <b>int</b>

The width of the spacing between icons in large icon mode, in pixels.


### -field cyLarge

Type: <b>int</b>

The height of the spacing between icons in large icon mode, in pixels.

