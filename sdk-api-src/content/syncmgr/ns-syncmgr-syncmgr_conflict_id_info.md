---
UID: NS:syncmgr.SYNCMGR_CONFLICT_ID_INFO
title: SYNCMGR_CONFLICT_ID_INFO
author: windows-sdk-content
description: Describes conflict ID information structure.
old-location: shell\SYNCMGR_CONFLICT_ID_INFO.htm
old-project: shell
ms.assetid: 9a54ef7e-0b22-436e-891b-80610ddaef00
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSYNCMGR_CONFLICT_ID_INFO, PSYNCMGR_CONFLICT_ID_INFO, PSYNCMGR_CONFLICT_ID_INFO structure pointer [Windows Shell], SYNCMGR_CONFLICT_ID_INFO, SYNCMGR_CONFLICT_ID_INFO structure [Windows Shell], _shell_SYNCMGR_CONFLICT_ID_INFO, shell.SYNCMGR_CONFLICT_ID_INFO, syncmgr/PSYNCMGR_CONFLICT_ID_INFO, syncmgr/SYNCMGR_CONFLICT_ID_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: syncmgr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SYNCMGR_CONFLICT_ID_INFO, *PSYNCMGR_CONFLICT_ID_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_CONFLICT_ID_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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

