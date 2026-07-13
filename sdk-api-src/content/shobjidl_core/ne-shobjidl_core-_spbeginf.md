---
UID: NE:shobjidl_core._SPBEGINF
title: _SPBEGINF (shobjidl_core.h)
description: Used by IActionProgress::Begin, these constants specify certain UI operations that are to be enabled or disabled.
helpviewer_keywords: ["SPBEGINF","SPBEGINF enumeration [Windows Shell]","SPBEGINF_AUTOTIME","SPBEGINF_MARQUEEPROGRESS","SPBEGINF_NOCANCELBUTTON","SPBEGINF_NOPROGRESSBAR","SPBEGINF_NORMAL","_SPBEGINF","shell.SPBEGINF_Constants","shell_SPBEGINF_Constants","shobjidl_core/SPBEGINF","shobjidl_core/SPBEGINF_AUTOTIME","shobjidl_core/SPBEGINF_MARQUEEPROGRESS","shobjidl_core/SPBEGINF_NOCANCELBUTTON","shobjidl_core/SPBEGINF_NOPROGRESSBAR","shobjidl_core/SPBEGINF_NORMAL"]
old-location: shell\SPBEGINF_Constants.htm
tech.root: shell
ms.assetid: dc5215ca-17c8-47c1-8059-f46400ff1d0f
ms.date: 12/05/2018
ms.keywords: SPBEGINF, SPBEGINF enumeration [Windows Shell], SPBEGINF_AUTOTIME, SPBEGINF_MARQUEEPROGRESS, SPBEGINF_NOCANCELBUTTON, SPBEGINF_NOPROGRESSBAR, SPBEGINF_NORMAL, _SPBEGINF, shell.SPBEGINF_Constants, shell_SPBEGINF_Constants, shobjidl_core/SPBEGINF, shobjidl_core/SPBEGINF_AUTOTIME, shobjidl_core/SPBEGINF_MARQUEEPROGRESS, shobjidl_core/SPBEGINF_NOCANCELBUTTON, shobjidl_core/SPBEGINF_NOPROGRESSBAR, shobjidl_core/SPBEGINF_NORMAL
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
req.product: Outlook Express 6.0
ms.custom: 19H1
f1_keywords:
 - _SPBEGINF
 - shobjidl_core/_SPBEGINF
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
 - SPBEGINF
---

# _SPBEGINF enumeration


## -description

Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin">IActionProgress::Begin</a>, these constants specify certain UI operations that are to be enabled or disabled.

## -enum-fields

### -field SPBEGINF_NORMAL:0

Indicates default progress behavior.

### -field SPBEGINF_AUTOTIME:0x2

Indicates that the progress UI should automatically update a text field with the amount of time remaining until the action completes.

### -field SPBEGINF_NOPROGRESSBAR:0x10

Indicates that the UI should not display a progress bar.

### -field SPBEGINF_MARQUEEPROGRESS:0x20

Indicates that the UI should use a marquee-style progress bar.

### -field SPBEGINF_NOCANCELBUTTON:0x40

Indicates that the UI should not include a <b>Cancel</b> button.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress">IActionProgress</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin">IActionProgress::Begin</a>
