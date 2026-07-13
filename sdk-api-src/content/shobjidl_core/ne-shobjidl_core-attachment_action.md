---
UID: NE:shobjidl_core.ATTACHMENT_ACTION
title: ATTACHMENT_ACTION (shobjidl_core.h)
description: Provides a set of flags to be used with IAttachmentExecute::Prompt to indicate the action to be performed upon user confirmation.
helpviewer_keywords: ["ATTACHMENT_ACTION","ATTACHMENT_ACTION enumeration [Windows Shell]","ATTACHMENT_ACTION_CANCEL","ATTACHMENT_ACTION_EXEC","ATTACHMENT_ACTION_SAVE","_win32_ATTACHMENT_ACTION","shell.ATTACHMENT_ACTION","shobjidl_core/ATTACHMENT_ACTION","shobjidl_core/ATTACHMENT_ACTION_CANCEL","shobjidl_core/ATTACHMENT_ACTION_EXEC","shobjidl_core/ATTACHMENT_ACTION_SAVE"]
old-location: shell\ATTACHMENT_ACTION.htm
tech.root: shell
ms.assetid: 2deeb14b-2665-4970-923c-9da1f561979f
ms.date: 12/05/2018
ms.keywords: ATTACHMENT_ACTION, ATTACHMENT_ACTION enumeration [Windows Shell], ATTACHMENT_ACTION_CANCEL, ATTACHMENT_ACTION_EXEC, ATTACHMENT_ACTION_SAVE, _win32_ATTACHMENT_ACTION, shell.ATTACHMENT_ACTION, shobjidl_core/ATTACHMENT_ACTION, shobjidl_core/ATTACHMENT_ACTION_CANCEL, shobjidl_core/ATTACHMENT_ACTION_EXEC, shobjidl_core/ATTACHMENT_ACTION_SAVE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: ATTACHMENT_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ATTACHMENT_ACTION
 - shobjidl_core/ATTACHMENT_ACTION
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
 - ATTACHMENT_ACTION
---

# ATTACHMENT_ACTION enumeration


## -description

Provides a set of flags to be used with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt">IAttachmentExecute::Prompt</a> to indicate the action to be performed upon user confirmation.

## -enum-fields

### -field ATTACHMENT_ACTION_CANCEL:0

Cancel

### -field ATTACHMENT_ACTION_SAVE:0x1

Save

### -field ATTACHMENT_ACTION_EXEC:0x2

Execute
