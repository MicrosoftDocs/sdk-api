---
UID: NE:shlobj_core.tagIESHORTCUTFLAGS
title: tagIESHORTCUTFLAGS
author: windows-sdk-content
description: Specifies how a shortcut should be handled by the browser.
old-location: shell\IESHORTCUTFLAGS.htm
tech.root: shell
ms.assetid: 0821a990-5cae-41b3-aebf-20be13b6e89b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IESHORTCUTFLAGS, IESHORTCUTFLAGS enumeration [Windows Shell], IESHORTCUT_BACKGROUNDTAB, IESHORTCUT_FORCENAVIGATE, IESHORTCUT_NEWBROWSER, IESHORTCUT_OPENNEWTAB, _shell_IESHORTCUTFLAGS, shell.IESHORTCUTFLAGS, shlobj_core/IESHORTCUTFLAGS, shlobj_core/IESHORTCUT_BACKGROUNDTAB, shlobj_core/IESHORTCUT_FORCENAVIGATE, shlobj_core/IESHORTCUT_NEWBROWSER, shlobj_core/IESHORTCUT_OPENNEWTAB, tagIESHORTCUTFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - IESHORTCUTFLAGS
product: Windows
targetos: Windows
req.typenames: IESHORTCUTFLAGS
req.redist: 
---

# tagIESHORTCUTFLAGS enumeration


## -description


Specifies how a shortcut should be handled by the browser.


## -enum-fields




### -field IESHORTCUT_NEWBROWSER

A new browser window should be opened for each shortcut.


### -field IESHORTCUT_OPENNEWTAB

The current or topmost browser window should open the link in a new foreground tab.


### -field IESHORTCUT_FORCENAVIGATE

The current or topmost browser window should open the link.


### -field IESHORTCUT_BACKGROUNDTAB

The current or topmost browser window should open the link in a new  background tab.

