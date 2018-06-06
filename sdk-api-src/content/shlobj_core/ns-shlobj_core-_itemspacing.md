---
UID: NS:shlobj_core._ITEMSPACING
title: "_ITEMSPACING"
author: windows-sdk-content
description: Stores the dimensions of the two possible sizes of icon spacing that are available for display:\_small and large. Used by IShellFolderView::GetItemSpacing.
old-location: shell\ITEMSPACING.htm
old-project: shell
ms.assetid: fcd7f3da-6aba-4683-bd5e-14a6b5f93cb5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITEMSPACING, ITEMSPACING structure [Windows Shell], _ITEMSPACING, _shell_ITEMSPACING, shell.ITEMSPACING, shlobj_core/ITEMSPACING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: ITEMSPACING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - ITEMSPACING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _ITEMSPACING structure


## -description


Stores the dimensions of the two possible sizes of icon spacing that are available for display: small and large. Used by <a href="https://msdn.microsoft.com/92450bc7-26e5-4061-90f7-eea0f0a4db09">IShellFolderView::GetItemSpacing</a>.


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

