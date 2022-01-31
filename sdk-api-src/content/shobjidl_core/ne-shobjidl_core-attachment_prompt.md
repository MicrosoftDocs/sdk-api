---
UID: NE:shobjidl_core.ATTACHMENT_PROMPT
title: ATTACHMENT_PROMPT (shobjidl_core.h)
description: Provides a set of flags to be used with IAttachmentExecute::Prompt to indicate the type of prompt UI to display.
helpviewer_keywords: ["ATTACHMENT_PROMPT","ATTACHMENT_PROMPT enumeration [Windows Shell]","ATTACHMENT_PROMPT_EXEC","ATTACHMENT_PROMPT_EXEC_OR_SAVE","ATTACHMENT_PROMPT_NONE","ATTACHMENT_PROMPT_SAVE","_win32_ATTACHMENT_PROMPT","shell.ATTACHMENT_PROMPT","shobjidl_core/ATTACHMENT_PROMPT","shobjidl_core/ATTACHMENT_PROMPT_EXEC","shobjidl_core/ATTACHMENT_PROMPT_EXEC_OR_SAVE","shobjidl_core/ATTACHMENT_PROMPT_NONE","shobjidl_core/ATTACHMENT_PROMPT_SAVE"]
old-location: shell\ATTACHMENT_PROMPT.htm
tech.root: shell
ms.assetid: a19bdff0-3b02-44f4-906a-2e1b85685c52
ms.date: 12/05/2018
ms.keywords: ATTACHMENT_PROMPT, ATTACHMENT_PROMPT enumeration [Windows Shell], ATTACHMENT_PROMPT_EXEC, ATTACHMENT_PROMPT_EXEC_OR_SAVE, ATTACHMENT_PROMPT_NONE, ATTACHMENT_PROMPT_SAVE, _win32_ATTACHMENT_PROMPT, shell.ATTACHMENT_PROMPT, shobjidl_core/ATTACHMENT_PROMPT, shobjidl_core/ATTACHMENT_PROMPT_EXEC, shobjidl_core/ATTACHMENT_PROMPT_EXEC_OR_SAVE, shobjidl_core/ATTACHMENT_PROMPT_NONE, shobjidl_core/ATTACHMENT_PROMPT_SAVE
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
req.typenames: ATTACHMENT_PROMPT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ATTACHMENT_PROMPT
 - shobjidl_core/ATTACHMENT_PROMPT
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
 - ATTACHMENT_PROMPT
---

# ATTACHMENT_PROMPT enumeration


## -description

Provides a set of flags to be used with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt">IAttachmentExecute::Prompt</a> to indicate the type of prompt UI to display.

## -enum-fields

### -field ATTACHMENT_PROMPT_NONE:0

Do not use.

### -field ATTACHMENT_PROMPT_SAVE:0x1

Displays a prompt asking whether the user would like to save the attachment.

### -field ATTACHMENT_PROMPT_EXEC:0x2

Displays a prompt asking whether the user would like to execute the attachment.

### -field ATTACHMENT_PROMPT_EXEC_OR_SAVE:0x3

Displays a prompt giving the user a choice of executing or saving the attachment.
