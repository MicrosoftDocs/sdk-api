---
UID: NE:shobjidl_core._EXPLORERPANESTATE
title: _EXPLORERPANESTATE (shobjidl_core.h)
description: Indicate flags used by IExplorerPaneVisibility::GetPaneState to get the current state of the given Windows Explorer pane.
helpviewer_keywords: ["EPS_DEFAULT_OFF","EPS_DEFAULT_ON","EPS_DONTCARE","EPS_FORCE","EPS_INITIALSTATE","EPS_STATEMASK","EXPLORERPANESTATE","EXPLORERPANESTATE enumeration [Windows Shell]","_EXPLORERPANESTATE","_shell_EXPLORERPANESTATE","shell.EXPLORERPANESTATE","shobjidl_core/EPS_DEFAULT_OFF","shobjidl_core/EPS_DEFAULT_ON","shobjidl_core/EPS_DONTCARE","shobjidl_core/EPS_FORCE","shobjidl_core/EPS_INITIALSTATE","shobjidl_core/EPS_STATEMASK","shobjidl_core/EXPLORERPANESTATE"]
old-location: shell\EXPLORERPANESTATE.htm
tech.root: shell
ms.assetid: 4caa2fe7-5bb3-4940-a429-fd32128eea84
ms.date: 12/05/2018
ms.keywords: EPS_DEFAULT_OFF, EPS_DEFAULT_ON, EPS_DONTCARE, EPS_FORCE, EPS_INITIALSTATE, EPS_STATEMASK, EXPLORERPANESTATE, EXPLORERPANESTATE enumeration [Windows Shell], _EXPLORERPANESTATE, _shell_EXPLORERPANESTATE, shell.EXPLORERPANESTATE, shobjidl_core/EPS_DEFAULT_OFF, shobjidl_core/EPS_DEFAULT_ON, shobjidl_core/EPS_DONTCARE, shobjidl_core/EPS_FORCE, shobjidl_core/EPS_INITIALSTATE, shobjidl_core/EPS_STATEMASK, shobjidl_core/EXPLORERPANESTATE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - _EXPLORERPANESTATE
 - shobjidl_core/_EXPLORERPANESTATE
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
 - EXPLORERPANESTATE
---

# _EXPLORERPANESTATE enumeration


## -description

Indicate flags used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate">IExplorerPaneVisibility::GetPaneState</a> to get the current state of the given Windows Explorer pane.

## -enum-fields

### -field EPS_DONTCARE:0

Do not make any modifications to the pane.

### -field EPS_DEFAULT_ON:0x1

Set the default state of the pane to "on", but respect any user-modified persisted state.

### -field EPS_DEFAULT_OFF:0x2

Set the default state of the pane to "off".

### -field EPS_STATEMASK:0xffff

Unused.

### -field EPS_INITIALSTATE:0x10000

Ignore any persisted state from the user, but the user can still modify the state.

### -field EPS_FORCE:0x20000

Users cannot modify the state, that is, they do not have the ability to show or hide the given pane. This option implies EPS_INITIALSTATE.
