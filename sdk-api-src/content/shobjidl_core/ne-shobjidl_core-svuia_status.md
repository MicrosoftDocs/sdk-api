---
UID: NE:shobjidl_core.SVUIA_STATUS
title: SVUIA_STATUS
author: windows-sdk-content
description: Used with the IBrowserService2::_UIActivateView method to set the state of a browser view.
old-location: shell\SVUIA_STATUS.htm
old-project: shell
ms.assetid: 04cb4259-4d16-44d0-8186-bce21ceab887
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SVUIA_ACTIVATE_FOCUS, SVUIA_ACTIVATE_NOFOCUS, SVUIA_DEACTIVATE, SVUIA_INPLACEACTIVATE, SVUIA_STATUS, SVUIA_STATUS enumeration [Windows Shell], _win32_SVUIA_STATUS, shell.SVUIA_STATUS, shobjidl_core/SVUIA_ACTIVATE_FOCUS, shobjidl_core/SVUIA_ACTIVATE_NOFOCUS, shobjidl_core/SVUIA_DEACTIVATE, shobjidl_core/SVUIA_INPLACEACTIVATE, shobjidl_core/SVUIA_STATUS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: SVUIA_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SVUIA_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SVUIA_STATUS enumeration


## -description


Used with the <a href="https://msdn.microsoft.com/9c8439f8-5931-4aca-8085-2707b6f964f0">IBrowserService2::_UIActivateView</a> method to set the state of a browser view.


## -enum-fields




### -field SVUIA_DEACTIVATE

The browser view has been deactivated.


### -field SVUIA_ACTIVATE_NOFOCUS

The browser view is activated and does not have focus.


### -field SVUIA_ACTIVATE_FOCUS

The browser view is activated and has focus.


### -field SVUIA_INPLACEACTIVATE

The browser view is activated in place.

