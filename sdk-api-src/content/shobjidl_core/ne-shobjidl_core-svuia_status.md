---
UID: NE:shobjidl_core.SVUIA_STATUS
title: SVUIA_STATUS (shobjidl_core.h)
description: Used with the IBrowserService2::_UIActivateView method to set the state of a browser view.
old-location: shell\SVUIA_STATUS.htm
tech.root: shell
ms.assetid: 04cb4259-4d16-44d0-8186-bce21ceab887
ms.date: 12/05/2018
ms.keywords: SVUIA_ACTIVATE_FOCUS, SVUIA_ACTIVATE_NOFOCUS, SVUIA_DEACTIVATE, SVUIA_INPLACEACTIVATE, SVUIA_STATUS, SVUIA_STATUS enumeration [Windows Shell], _win32_SVUIA_STATUS, shell.SVUIA_STATUS, shobjidl_core/SVUIA_ACTIVATE_FOCUS, shobjidl_core/SVUIA_ACTIVATE_NOFOCUS, shobjidl_core/SVUIA_DEACTIVATE, shobjidl_core/SVUIA_INPLACEACTIVATE, shobjidl_core/SVUIA_STATUS
ms.topic: enum
f1_keywords:
- shobjidl_core/SVUIA_STATUS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- shobjidl_core.h
api_name:
- SVUIA_STATUS
targetos: Windows
req.typenames: SVUIA_STATUS
req.redist: 
ms.custom: 19H1
---

# SVUIA_STATUS enumeration


## -description


Used with the <a href="https://docs.microsoft.com/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview">IBrowserService2::_UIActivateView</a> method to set the state of a browser view.


## -enum-fields




### -field SVUIA_DEACTIVATE

The browser view has been deactivated.


### -field SVUIA_ACTIVATE_NOFOCUS

The browser view is activated and does not have focus.


### -field SVUIA_ACTIVATE_FOCUS

The browser view is activated and has focus.


### -field SVUIA_INPLACEACTIVATE

The browser view is activated in place.

