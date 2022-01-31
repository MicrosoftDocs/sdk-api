---
UID: NE:shobjidl_core.FILE_USAGE_TYPE
title: FILE_USAGE_TYPE (shobjidl_core.h)
description: Constants used by IFileIsInUse::GetUsage to indicate how a file in use is being used.
helpviewer_keywords: ["FILE_USAGE_TYPE","FILE_USAGE_TYPE enumeration [Windows Shell]","FUT_EDITING","FUT_GENERIC","FUT_PLAYING","_shell_FILE_USAGE_TYPE","shell.FILE_USAGE_TYPE","shobjidl_core/FILE_USAGE_TYPE","shobjidl_core/FUT_EDITING","shobjidl_core/FUT_GENERIC","shobjidl_core/FUT_PLAYING"]
old-location: shell\FILE_USAGE_TYPE.htm
tech.root: shell
ms.assetid: 32b0e148-499a-401d-837c-8cea74cf9cac
ms.date: 12/05/2018
ms.keywords: FILE_USAGE_TYPE, FILE_USAGE_TYPE enumeration [Windows Shell], FUT_EDITING, FUT_GENERIC, FUT_PLAYING, _shell_FILE_USAGE_TYPE, shell.FILE_USAGE_TYPE, shobjidl_core/FILE_USAGE_TYPE, shobjidl_core/FUT_EDITING, shobjidl_core/FUT_GENERIC, shobjidl_core/FUT_PLAYING
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
req.typenames: FILE_USAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FILE_USAGE_TYPE
 - shobjidl_core/FILE_USAGE_TYPE
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
 - FILE_USAGE_TYPE
---

# FILE_USAGE_TYPE enumeration


## -description

Constants used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getusage">IFileIsInUse::GetUsage</a> to indicate how a file in use is being used.

## -enum-fields

### -field FUT_PLAYING:0

The file is being played by the process that has it open.

### -field FUT_EDITING

The file is being edited by the process that has it open.

### -field FUT_GENERIC

The file is open in the process for an unspecified action or an action that does not readily fit into the other two categories.

## -remarks

The interpretation of "playing" or "editing" is left to the application's implementation of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse">IFileIsInUse</a>. Generally, "playing" would refer to a media file while "editing" can refer to any file being altered in an application. However, the application itself best knows how to map these terms to its actions.
