---
UID: NS:shlobj_core._tagCOMPPOS
title: COMPPOS (shlobj_core.h)
description: Holds information about a component's position and size.
helpviewer_keywords: ["*LPCOMPPOS","COMPPOS","COMPPOS structure [Windows Shell]","LPCOMPPOS","LPCOMPPOS structure pointer [Windows Shell]","_tagCOMPPOS","_win32_COMPPOS","shell.COMPPOS","shlobj_core/COMPPOS","shlobj_core/LPCOMPPOS"]
old-location: shell\COMPPOS.htm
tech.root: shell
ms.assetid: 622bdf51-d605-4eb9-a692-09be028bbff8
ms.date: 12/05/2018
ms.keywords: '*LPCOMPPOS, COMPPOS, COMPPOS structure [Windows Shell], LPCOMPPOS, LPCOMPPOS structure pointer [Windows Shell], _tagCOMPPOS, _win32_COMPPOS, shell.COMPPOS, shlobj_core/COMPPOS, shlobj_core/LPCOMPPOS'
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
req.typenames: COMPPOS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagCOMPPOS
 - shlobj_core/_tagCOMPPOS
 - COMPPOS
 - shlobj_core/COMPPOS
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
 - COMPPOS
---

# COMPPOS structure


## -description

Holds information about a component's position and size.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size of the structure.

### -field iLeft

Type: <b>int</b>

The left edge of the top-left corner in screen coordinates. Set to COMPONENT_DEFAULT_LEFT to let the Shell decide the position.

### -field iTop

Type: <b>int</b>

The top of the top-left corner in screen coordinates. Set to COMPONENT_DEFAULT_TOP to let the Shell decide the position.

### -field dwWidth

Type: <b>DWORD</b>

The width, in pixels.

### -field dwHeight

Type: <b>DWORD</b>

The height, in pixels.

### -field izIndex

Type: <b>int</b>

The z-order of the component.

### -field fCanResize

Type: <b>BOOL</b>

Set to <b>TRUE</b> if the component is resizable, <b>FALSE</b> if not.

### -field fCanResizeX

Type: <b>BOOL</b>

Set to <b>TRUE</b> if the component is resizable in the x direction, <b>FALSE</b> if not.

### -field fCanResizeY

Type: <b>BOOL</b>

Set to <b>TRUE</b> if the component is resizable in the y direction, <b>FALSE</b> if not.

### -field iPreferredLeftPercent

Type: <b>int</b>

The left edge of the upper-left corner as a percentage of screen width.

### -field iPreferredTopPercent

Type: <b>int</b>

The top of the upper-left corner as a percentage of screen width.

