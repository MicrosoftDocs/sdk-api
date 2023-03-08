---
UID: NE:uiribbon.UI_OWNERSHIP
title: UI_OWNERSHIP (uiribbon.h)
description: Specifies values that identify the ownership conditions under which an image is created by the Windows Ribbon framework.
helpviewer_keywords: ["UI_OWNERSHIP","UI_OWNERSHIP enumeration [Windows Ribbon]","UI_OWNERSHIP_COPY","UI_OWNERSHIP_TRANSFER","scenicintent_UI_OWNERSHIP","uiribbon/UI_OWNERSHIP","uiribbon/UI_OWNERSHIP_COPY","uiribbon/UI_OWNERSHIP_TRANSFER","windowsribbon.windowsribbon_ui_ownership"]
old-location: windowsribbon\windowsribbon_ui_ownership.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\enums\ui_ownership.htm
ms.date: 12/05/2018
ms.keywords: UI_OWNERSHIP, UI_OWNERSHIP enumeration [Windows Ribbon], UI_OWNERSHIP_COPY, UI_OWNERSHIP_TRANSFER, scenicintent_UI_OWNERSHIP, uiribbon/UI_OWNERSHIP, uiribbon/UI_OWNERSHIP_COPY, uiribbon/UI_OWNERSHIP_TRANSFER, windowsribbon.windowsribbon_ui_ownership
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UI_OWNERSHIP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UI_OWNERSHIP
 - uiribbon/UI_OWNERSHIP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uiribbon.h
api_name:
 - UI_OWNERSHIP
---

# UI_OWNERSHIP enumeration


## -description

Specifies values that identify the ownership conditions under which an image is created by the Windows Ribbon framework.

## -enum-fields

### -field UI_OWNERSHIP_TRANSFER:0

The handle to the bitmap (HBITMAP) is owned by the Ribbon framework 
			through the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage">IUIImage</a> object.

### -field UI_OWNERSHIP_COPY:1

A copy of the HBITMAP is created by the Ribbon framework through 
			the <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage">IUIImage</a> object. The host application still owns the HBITMAP.

## -see-also

<a href="/windows/desktop/windowsribbon/windowsribbon-reference-enumerations">Constants and Enumerations</a>



<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiimagefrombitmap-createimage">IUIImageFromBitmap::CreateImage</a>
