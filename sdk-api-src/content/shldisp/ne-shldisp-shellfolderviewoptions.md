---
UID: NE:shldisp.ShellFolderViewOptions
title: ShellFolderViewOptions (shldisp.h)
description: Specifies the view options returned by the ViewOptions property.
helpviewer_keywords: ["SFVVO_DESKTOPHTML","SFVVO_DOUBLECLICKINWEBVIEW","SFVVO_SHOWALLOBJECTS","SFVVO_SHOWCOMPCOLOR","SFVVO_SHOWEXTENSIONS","SFVVO_SHOWSYSFILES","SFVVO_WIN95CLASSIC","ShellFolderViewOptions","ShellFolderViewOptions enumeration [Windows Shell]","_win32_ShellFolderViewOptions","shell.ShellFolderViewOptions","shldisp/SFVVO_DESKTOPHTML","shldisp/SFVVO_DOUBLECLICKINWEBVIEW","shldisp/SFVVO_SHOWALLOBJECTS","shldisp/SFVVO_SHOWCOMPCOLOR","shldisp/SFVVO_SHOWEXTENSIONS","shldisp/SFVVO_SHOWSYSFILES","shldisp/SFVVO_WIN95CLASSIC","shldisp/ShellFolderViewOptions"]
old-location: shell\ShellFolderViewOptions.htm
tech.root: shell
ms.assetid: 7028ff38-7596-4126-aa98-c0be519243c9
ms.date: 12/05/2018
ms.keywords: SFVVO_DESKTOPHTML, SFVVO_DOUBLECLICKINWEBVIEW, SFVVO_SHOWALLOBJECTS, SFVVO_SHOWCOMPCOLOR, SFVVO_SHOWEXTENSIONS, SFVVO_SHOWSYSFILES, SFVVO_WIN95CLASSIC, ShellFolderViewOptions, ShellFolderViewOptions enumeration [Windows Shell], _win32_ShellFolderViewOptions, shell.ShellFolderViewOptions, shldisp/SFVVO_DESKTOPHTML, shldisp/SFVVO_DOUBLECLICKINWEBVIEW, shldisp/SFVVO_SHOWALLOBJECTS, shldisp/SFVVO_SHOWCOMPCOLOR, shldisp/SFVVO_SHOWEXTENSIONS, shldisp/SFVVO_SHOWSYSFILES, shldisp/SFVVO_WIN95CLASSIC, shldisp/ShellFolderViewOptions
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ShellFolderViewOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShellFolderViewOptions
 - shldisp/ShellFolderViewOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shldisp.h
api_name:
 - ShellFolderViewOptions
---

# ShellFolderViewOptions enumeration


## -description

Specifies the view options returned by the <a href="/windows/desktop/shell/shellfolderview-viewoptions">ViewOptions</a> property.

## -enum-fields

### -field SFVVO_SHOWALLOBJECTS:0x1

0x0001. The <b>Show All Files</b> option is enabled.

### -field SFVVO_SHOWEXTENSIONS:0x2

0x0002. The <b>Hide extensions for known file types</b> option is disabled.

### -field SFVVO_SHOWCOMPCOLOR:0x8

0x0008. The <b>Display Compressed Files and Folders with Alternate Color</b> option is enabled.

### -field SFVVO_SHOWSYSFILES:0x20

0x0020. The <b>Do Not Show Hidden Files</b> option is enabled.

### -field SFVVO_WIN95CLASSIC:0x40

0x0040. The <b>Classic Style</b> option is enabled.

### -field SFVVO_DOUBLECLICKINWEBVIEW:0x80

0x0080. The <b>Double-Click to Open an Item</b> option is enabled.

### -field SFVVO_DESKTOPHTML:0x200

0x0200. The <b>Active Desktop – View as Web Page</b> option is enabled.
