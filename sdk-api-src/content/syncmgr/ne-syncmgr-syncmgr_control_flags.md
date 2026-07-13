---
UID: NE:syncmgr.SYNCMGR_CONTROL_FLAGS
title: SYNCMGR_CONTROL_FLAGS (syncmgr.h)
description: Specifies how an operation requested on certain methods of ISyncMgrControl should be performed.
helpviewer_keywords: ["SYNCMGR_CF_NONE","SYNCMGR_CF_NOUI","SYNCMGR_CF_NOWAIT","SYNCMGR_CF_VALID","SYNCMGR_CF_WAIT","SYNCMGR_CONTROL_FLAGS","SYNCMGR_CONTROL_FLAGS enumeration [Windows Shell]","shell.SYNCMGR_CONTROL_FLAGS","shell_SYNCMGR_CONTROL_FLAGS","syncmgr/SYNCMGR_CF_NONE","syncmgr/SYNCMGR_CF_NOUI","syncmgr/SYNCMGR_CF_NOWAIT","syncmgr/SYNCMGR_CF_VALID","syncmgr/SYNCMGR_CF_WAIT","syncmgr/SYNCMGR_CONTROL_FLAGS"]
old-location: shell\SYNCMGR_CONTROL_FLAGS.htm
tech.root: shell
ms.assetid: cfba36ba-8cbd-41ae-91ae-e568546508b9
ms.date: 12/05/2018
ms.keywords: SYNCMGR_CF_NONE, SYNCMGR_CF_NOUI, SYNCMGR_CF_NOWAIT, SYNCMGR_CF_VALID, SYNCMGR_CF_WAIT, SYNCMGR_CONTROL_FLAGS, SYNCMGR_CONTROL_FLAGS enumeration [Windows Shell], shell.SYNCMGR_CONTROL_FLAGS, shell_SYNCMGR_CONTROL_FLAGS, syncmgr/SYNCMGR_CF_NONE, syncmgr/SYNCMGR_CF_NOUI, syncmgr/SYNCMGR_CF_NOWAIT, syncmgr/SYNCMGR_CF_VALID, syncmgr/SYNCMGR_CF_WAIT, syncmgr/SYNCMGR_CONTROL_FLAGS
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SYNCMGR_CONTROL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_CONTROL_FLAGS
 - syncmgr/SYNCMGR_CONTROL_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_CONTROL_FLAGS
---

# SYNCMGR_CONTROL_FLAGS enumeration


## -description

Specifies how an operation requested on certain methods of <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a> should be performed.

## -enum-fields

### -field SYNCMGR_CF_NONE:0

Perform the operation not using any of the other flags in this enumeration.

### -field SYNCMGR_CF_NOWAIT:0

Perform the operation asynchronously.

### -field SYNCMGR_CF_WAIT:0x1

Perform the operation synchronously.

### -field SYNCMGR_CF_NOUI:0x2

Perform the operation without asking the sync handler to display the UI during the operation.

### -field SYNCMGR_CF_VALID:0x3

A mask used to determine valid <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> flags.
