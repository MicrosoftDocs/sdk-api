---
UID: NS:syncmgr.SYNCMGR_CONFLICT_ID_INFO
title: SYNCMGR_CONFLICT_ID_INFO (syncmgr.h)
description: Describes conflict ID information structure.
helpviewer_keywords: ["*PSYNCMGR_CONFLICT_ID_INFO","PSYNCMGR_CONFLICT_ID_INFO","PSYNCMGR_CONFLICT_ID_INFO structure pointer [Windows Shell]","SYNCMGR_CONFLICT_ID_INFO","SYNCMGR_CONFLICT_ID_INFO structure [Windows Shell]","_shell_SYNCMGR_CONFLICT_ID_INFO","shell.SYNCMGR_CONFLICT_ID_INFO","syncmgr/PSYNCMGR_CONFLICT_ID_INFO","syncmgr/SYNCMGR_CONFLICT_ID_INFO"]
old-location: shell\SYNCMGR_CONFLICT_ID_INFO.htm
tech.root: shell
ms.assetid: 9a54ef7e-0b22-436e-891b-80610ddaef00
ms.date: 12/05/2018
ms.keywords: '*PSYNCMGR_CONFLICT_ID_INFO, PSYNCMGR_CONFLICT_ID_INFO, PSYNCMGR_CONFLICT_ID_INFO structure pointer [Windows Shell], SYNCMGR_CONFLICT_ID_INFO, SYNCMGR_CONFLICT_ID_INFO structure [Windows Shell], _shell_SYNCMGR_CONFLICT_ID_INFO, shell.SYNCMGR_CONFLICT_ID_INFO, syncmgr/PSYNCMGR_CONFLICT_ID_INFO, syncmgr/SYNCMGR_CONFLICT_ID_INFO'
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
req.typenames: SYNCMGR_CONFLICT_ID_INFO, *PSYNCMGR_CONFLICT_ID_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_CONFLICT_ID_INFO
 - syncmgr/SYNCMGR_CONFLICT_ID_INFO
 - PSYNCMGR_CONFLICT_ID_INFO
 - syncmgr/PSYNCMGR_CONFLICT_ID_INFO
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
 - SYNCMGR_CONFLICT_ID_INFO
---

# SYNCMGR_CONFLICT_ID_INFO structure


## -description

Describes conflict ID information structure.

## -struct-fields

### -field pblobID

Type: <b>BYTE_BLOB*</b>

A pointer to a blob used for comparison.

### -field pblobExtra

Type: <b>BYTE_BLOB*</b>

A pointer to extra data used to initialize conflict objects.

