---
UID: NS:shlobj_core._tagCOMPONENT
title: COMPONENT (shlobj_core.h)
description: Used by Windows 2000 to hold information about a component. This structure replaces the IE4COMPONENT structure.
helpviewer_keywords: ["*LPCOMPONENT","COMPONENT","COMPONENT structure [Windows Shell]","COMP_TYPE_CONTROL","COMP_TYPE_HTMLDOC","COMP_TYPE_PICTURE","COMP_TYPE_WEBSITE","IS_FULLSCREEN","IS_NORMAL","IS_SPLIT","LPCOMPONENT","LPCOMPONENT structure pointer [Windows Shell]","_tagCOMPONENT","_win32_COMPONENT","shell.COMPONENT","shlobj_core/COMPONENT","shlobj_core/LPCOMPONENT"]
old-location: shell\COMPONENT.htm
tech.root: shell
ms.assetid: 2692a2d6-1d33-410f-987c-8388c636cae6
ms.date: 12/05/2018
ms.keywords: '*LPCOMPONENT, COMPONENT, COMPONENT structure [Windows Shell], COMP_TYPE_CONTROL, COMP_TYPE_HTMLDOC, COMP_TYPE_PICTURE, COMP_TYPE_WEBSITE, IS_FULLSCREEN, IS_NORMAL, IS_SPLIT, LPCOMPONENT, LPCOMPONENT structure pointer [Windows Shell], _tagCOMPONENT, _win32_COMPONENT, shell.COMPONENT, shlobj_core/COMPONENT, shlobj_core/LPCOMPONENT'
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: COMPONENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagCOMPONENT
 - shlobj_core/_tagCOMPONENT
 - COMPONENT
 - shlobj_core/COMPONENT
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
 - COMPONENT
---

# COMPONENT structure


## -description

Used by Windows 2000 to hold information about a component. This structure replaces the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-ie4component">IE4COMPONENT</a> structure.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size of the structure.

### -field dwID

Type: <b>DWORD</b>

Reserved. Set to zero.

### -field iComponentType

Type: <b>int</b>

The component type. It can take one of the following values.



#### COMP_TYPE_HTMLDOC

HTML document



#### COMP_TYPE_PICTURE

Picture



#### COMP_TYPE_WEBSITE

Website



#### COMP_TYPE_CONTROL

ActiveX control. This value is valid only for <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem">IActiveDesktop::AddDesktopItem</a>.

### -field fChecked

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component is enabled, or <b>FALSE</b> if it's not.

### -field fDirty

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component has been modified and not yet saved to disk. It will be set to <b>FALSE</b> if the component has not been modified, or if it has been modified and saved to disk.

### -field fNoScroll

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component is scrollable, or <b>FALSE</b> if not.

### -field cpPos

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-comppos">COMPPOS</a></b>

A <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-comppos">COMPPOS</a> structure containing position and size information.

### -field wszFriendlyName

Type: <b>WCHAR[MAX_PATH]</b>

The component's friendly name.

### -field wszSource

Type: <b>WCHAR[INTERNET_MAX_URL_LENGTH]</b>

The component's URL.

### -field wszSubscribedURL

Type: <b>WCHAR[INTERNET_MAX_URL_LENGTH]</b>

The subscribed URL.

### -field dwCurItemState

Type: <b>DWORD</b>

The current state of the component. It can take one of the following values.



#### IS_NORMAL

Normal screen



#### IS_FULLSCREEN

Full screen



#### IS_SPLIT

Split screen

### -field csiOriginal

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-compstateinfo">COMPSTATEINFO</a></b>

A <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-compstateinfo">COMPSTATEINFO</a> structure with the state of the component when it was first added.

### -field csiRestored

Type: <b><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-compstateinfo">COMPSTATEINFO</a></b>

A <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-compstateinfo">COMPSTATEINFO</a> structure with the restored state of the component.