---
UID: NE:shlobj_core.tagIESHORTCUTFLAGS
title: IESHORTCUTFLAGS (shlobj_core.h)
description: Specifies how a shortcut should be handled by the browser.
helpviewer_keywords: ["IESHORTCUTFLAGS","IESHORTCUTFLAGS enumeration [Windows Shell]","IESHORTCUT_BACKGROUNDTAB","IESHORTCUT_FORCENAVIGATE","IESHORTCUT_NEWBROWSER","IESHORTCUT_OPENNEWTAB","_shell_IESHORTCUTFLAGS","shell.IESHORTCUTFLAGS","shlobj_core/IESHORTCUTFLAGS","shlobj_core/IESHORTCUT_BACKGROUNDTAB","shlobj_core/IESHORTCUT_FORCENAVIGATE","shlobj_core/IESHORTCUT_NEWBROWSER","shlobj_core/IESHORTCUT_OPENNEWTAB"]
old-location: shell\IESHORTCUTFLAGS.htm
tech.root: shell
ms.assetid: 0821a990-5cae-41b3-aebf-20be13b6e89b
ms.date: 12/05/2018
ms.keywords: IESHORTCUTFLAGS, IESHORTCUTFLAGS enumeration [Windows Shell], IESHORTCUT_BACKGROUNDTAB, IESHORTCUT_FORCENAVIGATE, IESHORTCUT_NEWBROWSER, IESHORTCUT_OPENNEWTAB, _shell_IESHORTCUTFLAGS, shell.IESHORTCUTFLAGS, shlobj_core/IESHORTCUTFLAGS, shlobj_core/IESHORTCUT_BACKGROUNDTAB, shlobj_core/IESHORTCUT_FORCENAVIGATE, shlobj_core/IESHORTCUT_NEWBROWSER, shlobj_core/IESHORTCUT_OPENNEWTAB
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IESHORTCUTFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIESHORTCUTFLAGS
 - shlobj_core/tagIESHORTCUTFLAGS
 - IESHORTCUTFLAGS
 - shlobj_core/IESHORTCUTFLAGS
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
 - IESHORTCUTFLAGS
---

# IESHORTCUTFLAGS enumeration


## -description

Specifies how a shortcut should be handled by the browser.

## -enum-fields

### -field IESHORTCUT_NEWBROWSER:0x01

A new browser window should be opened for each shortcut.

### -field IESHORTCUT_OPENNEWTAB:0x02

The current or topmost browser window should open the link in a new foreground tab.

### -field IESHORTCUT_FORCENAVIGATE:0x04

The current or topmost browser window should open the link.

### -field IESHORTCUT_BACKGROUNDTAB:0x08

The current or topmost browser window should open the link in a new  background tab.

