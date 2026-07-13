---
UID: NE:shobjidl_core.SVUIA_STATUS
title: SVUIA_STATUS (shobjidl_core.h)
description: Used with the IBrowserService2::_UIActivateView method to set the state of a browser view.
helpviewer_keywords: ["SVUIA_ACTIVATE_FOCUS","SVUIA_ACTIVATE_NOFOCUS","SVUIA_DEACTIVATE","SVUIA_INPLACEACTIVATE","SVUIA_STATUS","SVUIA_STATUS enumeration [Windows Shell]","_win32_SVUIA_STATUS","shell.SVUIA_STATUS","shobjidl_core/SVUIA_ACTIVATE_FOCUS","shobjidl_core/SVUIA_ACTIVATE_NOFOCUS","shobjidl_core/SVUIA_DEACTIVATE","shobjidl_core/SVUIA_INPLACEACTIVATE","shobjidl_core/SVUIA_STATUS"]
old-location: shell\SVUIA_STATUS.htm
tech.root: shell
ms.assetid: 04cb4259-4d16-44d0-8186-bce21ceab887
ms.date: 12/05/2018
ms.keywords: SVUIA_ACTIVATE_FOCUS, SVUIA_ACTIVATE_NOFOCUS, SVUIA_DEACTIVATE, SVUIA_INPLACEACTIVATE, SVUIA_STATUS, SVUIA_STATUS enumeration [Windows Shell], _win32_SVUIA_STATUS, shell.SVUIA_STATUS, shobjidl_core/SVUIA_ACTIVATE_FOCUS, shobjidl_core/SVUIA_ACTIVATE_NOFOCUS, shobjidl_core/SVUIA_DEACTIVATE, shobjidl_core/SVUIA_INPLACEACTIVATE, shobjidl_core/SVUIA_STATUS
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SVUIA_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SVUIA_STATUS
 - shobjidl_core/SVUIA_STATUS
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
 - SVUIA_STATUS
---

# SVUIA_STATUS enumeration


## -description

Used with the <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview">IBrowserService2::_UIActivateView</a> method to set the state of a browser view.

## -enum-fields

### -field SVUIA_DEACTIVATE:0

The browser view has been deactivated.

### -field SVUIA_ACTIVATE_NOFOCUS:1

The browser view is activated and does not have focus.

### -field SVUIA_ACTIVATE_FOCUS:2

The browser view is activated and has focus.

### -field SVUIA_INPLACEACTIVATE:3

The browser view is activated in place.

