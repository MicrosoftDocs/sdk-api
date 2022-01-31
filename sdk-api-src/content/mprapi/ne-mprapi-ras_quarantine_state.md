---
UID: NE:mprapi._RAS_QUARANTINE_STATE
title: RAS_QUARANTINE_STATE (mprapi.h)
description: The RAS_QUARANTINE_STATE enumerated type indicates the quarantine state of a client connection.
helpviewer_keywords: ["RAS_QUARANTINE_STATE","RAS_QUARANTINE_STATE enumeration [RAS]","RAS_QUAR_STATE_NORMAL","RAS_QUAR_STATE_NOT_CAPABLE","RAS_QUAR_STATE_PROBATION","RAS_QUAR_STATE_QUARANTINE","mprapi/RAS_QUARANTINE_STATE","mprapi/RAS_QUAR_STATE_NORMAL","mprapi/RAS_QUAR_STATE_NOT_CAPABLE","mprapi/RAS_QUAR_STATE_PROBATION","mprapi/RAS_QUAR_STATE_QUARANTINE","rras.ras_quarantine_state"]
old-location: rras\ras_quarantine_state.htm
tech.root: RRAS
ms.assetid: df0193c0-a40b-464f-8c82-08d1fe66fdf9
ms.date: 12/05/2018
ms.keywords: RAS_QUARANTINE_STATE, RAS_QUARANTINE_STATE enumeration [RAS], RAS_QUAR_STATE_NORMAL, RAS_QUAR_STATE_NOT_CAPABLE, RAS_QUAR_STATE_PROBATION, RAS_QUAR_STATE_QUARANTINE, mprapi/RAS_QUARANTINE_STATE, mprapi/RAS_QUAR_STATE_NORMAL, mprapi/RAS_QUAR_STATE_NOT_CAPABLE, mprapi/RAS_QUAR_STATE_PROBATION, mprapi/RAS_QUAR_STATE_QUARANTINE, rras.ras_quarantine_state
req.header: mprapi.h
req.include-header: 
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
targetos: Windows
req.typenames: RAS_QUARANTINE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RAS_QUARANTINE_STATE
 - mprapi/_RAS_QUARANTINE_STATE
 - RAS_QUARANTINE_STATE
 - mprapi/RAS_QUARANTINE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - RAS_QUARANTINE_STATE
---

# RAS_QUARANTINE_STATE enumeration


## -description

The 
<b>RAS_QUARANTINE_STATE</b> enumerated type indicates the quarantine state of a client connection.

## -enum-fields

### -field RAS_QUAR_STATE_NORMAL:0

The connection state is normal.

### -field RAS_QUAR_STATE_QUARANTINE:1

The connection is quarantined.

### -field RAS_QUAR_STATE_PROBATION:2

The connection is in probation.

### -field RAS_QUAR_STATE_NOT_CAPABLE:3

The connection state is unknown.

## -see-also

<a href="/windows/desktop/RRAS/ras-administration-enumerations">RAS Administration Enumerated Types</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
