---
UID: NE:shobjidl_core.PDOPSTATUS
title: PDOPSTATUS (shobjidl_core.h)
description: Provides operation status flags.
helpviewer_keywords: ["PDOPSTATUS","PDOPSTATUS enumeration [Windows Properties]","PDOPS_CANCELLED","PDOPS_ERRORS","PDOPS_PAUSED","PDOPS_RUNNING","PDOPS_STOPPED","_shell_PDOPSTATUS","properties.PDOPSTATUS","shell.PDOPSTATUS","shobjidl_core/PDOPSTATUS","shobjidl_core/PDOPS_CANCELLED","shobjidl_core/PDOPS_ERRORS","shobjidl_core/PDOPS_PAUSED","shobjidl_core/PDOPS_RUNNING","shobjidl_core/PDOPS_STOPPED"]
old-location: properties\PDOPSTATUS.htm
tech.root: properties
ms.assetid: f9fd5cbe-2cb7-4ae7-9cf2-f8545095eec8
ms.date: 12/05/2018
ms.keywords: PDOPSTATUS, PDOPSTATUS enumeration [Windows Properties], PDOPS_CANCELLED, PDOPS_ERRORS, PDOPS_PAUSED, PDOPS_RUNNING, PDOPS_STOPPED, _shell_PDOPSTATUS, properties.PDOPSTATUS, shell.PDOPSTATUS, shobjidl_core/PDOPSTATUS, shobjidl_core/PDOPS_CANCELLED, shobjidl_core/PDOPS_ERRORS, shobjidl_core/PDOPS_PAUSED, shobjidl_core/PDOPS_RUNNING, shobjidl_core/PDOPS_STOPPED
req.header: shobjidl_core.h
req.include-header: 
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
req.typenames: PDOPSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDOPSTATUS
 - shobjidl_core/PDOPSTATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - PDOPSTATUS
---

# PDOPSTATUS enumeration


## -description

Provides operation status flags.

## -enum-fields

### -field PDOPS_RUNNING:1

Operation is running, no user intervention.

### -field PDOPS_PAUSED:2

Operation has been paused by the user.

### -field PDOPS_CANCELLED:3

Operation has been canceled by the user - now go undo.

### -field PDOPS_STOPPED:4

Operation has been stopped by the user - terminate completely.

### -field PDOPS_ERRORS:5

Operation has gone as far as it can go without throwing error dialogs.

