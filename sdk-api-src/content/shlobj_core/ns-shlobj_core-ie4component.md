---
UID: NS:shlobj_core._tagIE4COMPONENT
title: IE4COMPONENT (shlobj_core.h)
description: Used by Microsoft Internet Explorer 4.0 and Microsoft Internet Explorer 4.01 to hold information about a component. With Windows 2000, it is replaced by the COMPONENT structure.
helpviewer_keywords: ["*LPIE4COMPONENT","COMP_TYPE_CONTROL","COMP_TYPE_HTMLDOC","COMP_TYPE_PICTURE","COMP_TYPE_WEBSITE","IE4COMPONENT","IE4COMPONENT structure [Windows Shell]","LPIE4COMPONENT","LPIE4COMPONENT structure pointer [Windows Shell]","_shell_IE4COMPONENT","_tagIE4COMPONENT","shell.IE4COMPONENT","shlobj_core/IE4COMPONENT","shlobj_core/LPIE4COMPONENT"]
old-location: shell\IE4COMPONENT.htm
tech.root: shell
ms.assetid: 5fcb2853-271b-4fcc-a3ea-0c2c6dd68195
ms.date: 12/05/2018
ms.keywords: '*LPIE4COMPONENT, COMP_TYPE_CONTROL, COMP_TYPE_HTMLDOC, COMP_TYPE_PICTURE, COMP_TYPE_WEBSITE, IE4COMPONENT, IE4COMPONENT structure [Windows Shell], LPIE4COMPONENT, LPIE4COMPONENT structure pointer [Windows Shell], _shell_IE4COMPONENT, _tagIE4COMPONENT, shell.IE4COMPONENT, shlobj_core/IE4COMPONENT, shlobj_core/LPIE4COMPONENT'
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
req.typenames: IE4COMPONENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagIE4COMPONENT
 - shlobj_core/_tagIE4COMPONENT
 - IE4COMPONENT
 - shlobj_core/IE4COMPONENT
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
 - IE4COMPONENT
---

# IE4COMPONENT structure


## -description

Used by Microsoft Internet Explorer 4.0 and Microsoft Internet Explorer 4.01 to hold information about a component. With Windows 2000, it is replaced by the <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-component">COMPONENT</a> structure.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

The size of the structure.

### -field dwID

Type: <b>DWORD</b>

Reserved. Set to zero.

### -field iComponentType

Type: <b>int</b>

The component type. It can be set to one of these values: 



#### COMP_TYPE_HTMLDOC



#### COMP_TYPE_PICTURE



#### COMP_TYPE_WEBSITE



#### COMP_TYPE_CONTROL

### -field fChecked

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component is enabled, or <b>FALSE</b> if not.

### -field fDirty

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component has been modified and not yet saved to disk. It will be set to <b>FALSE</b> if the component has not been modified, or if it has been modified and saved to disk.

### -field fNoScroll

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if the component is scrollable, or <b>FALSE</b> if it's not.

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

The URL that a user has been subscribed to.