---
UID: NE:projectedfslib.PRJ_COMPLETE_COMMAND_TYPE
title: PRJ_COMPLETE_COMMAND_TYPE (projectedfslib.h)
description: Specifies command types.
helpviewer_keywords: ["PRJ_COMPLETE_COMMAND_TYPE","PRJ_COMPLETE_COMMAND_TYPE enumeration","PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION","PRJ_COMPLETE_COMMAND_TYPE_NOTIFICATION","ProjFS.prj_complete_command_type","projectedfslib/PRJ_COMPLETE_COMMAND_TYPE","projectedfslib/PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION","projectedfslib/PRJ_COMPLETE_COMMAND_TYPE_NOTIFICATION"]
old-location: projfs\prj_complete_command_type.htm
tech.root: ProjFS
ms.assetid: AE9CD44C-0E68-4E35-8A7E-89B33E796AF0
ms.date: 12/05/2018
ms.keywords: PRJ_COMPLETE_COMMAND_TYPE, PRJ_COMPLETE_COMMAND_TYPE enumeration, PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION, PRJ_COMPLETE_COMMAND_TYPE_NOTIFICATION, ProjFS.prj_complete_command_type, projectedfslib/PRJ_COMPLETE_COMMAND_TYPE, projectedfslib/PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION, projectedfslib/PRJ_COMPLETE_COMMAND_TYPE_NOTIFICATION
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: PRJ_COMPLETE_COMMAND_TYPE
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_COMPLETE_COMMAND_TYPE
 - projectedfslib/PRJ_COMPLETE_COMMAND_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_COMPLETE_COMMAND_TYPE
---

# PRJ_COMPLETE_COMMAND_TYPE enumeration


## -description

Specifies command types.

## -enum-fields

### -field PRJ_COMPLETE_COMMAND_TYPE_NOTIFICATION:1

The provider is completing a call to its <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb">PRJ_NOTIFICATION_CB</a> callback.

### -field PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION:2

The provider is completing a call to its <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback.
