---
UID: NE:slpublic._SL_GENUINE_STATE
title: SL_GENUINE_STATE (slpublic.h)
description: Specifies the state of an application installation.
helpviewer_keywords: ["SL_GENUINE_STATE","SL_GENUINE_STATE enumeration [Security]","SL_GEN_STATE_INVALID_LICENSE","SL_GEN_STATE_IS_GENUINE","SL_GEN_STATE_LAST","SL_GEN_STATE_OFFLINE","SL_GEN_STATE_TAMPERED","security.sl_genuine_state","slpublic/SL_GENUINE_STATE","slpublic/SL_GEN_STATE_INVALID_LICENSE","slpublic/SL_GEN_STATE_IS_GENUINE","slpublic/SL_GEN_STATE_LAST","slpublic/SL_GEN_STATE_OFFLINE","slpublic/SL_GEN_STATE_TAMPERED"]
old-location: security\sl_genuine_state.htm
tech.root: security
ms.assetid: 3be69be1-289c-466a-9271-5309fd1319fe
ms.date: 12/05/2018
ms.keywords: SL_GENUINE_STATE, SL_GENUINE_STATE enumeration [Security], SL_GEN_STATE_INVALID_LICENSE, SL_GEN_STATE_IS_GENUINE, SL_GEN_STATE_LAST, SL_GEN_STATE_OFFLINE, SL_GEN_STATE_TAMPERED, security.sl_genuine_state, slpublic/SL_GENUINE_STATE, slpublic/SL_GEN_STATE_INVALID_LICENSE, slpublic/SL_GEN_STATE_IS_GENUINE, slpublic/SL_GEN_STATE_LAST, slpublic/SL_GEN_STATE_OFFLINE, slpublic/SL_GEN_STATE_TAMPERED
req.header: slpublic.h
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
req.typenames: SL_GENUINE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SL_GENUINE_STATE
 - slpublic/_SL_GENUINE_STATE
 - SL_GENUINE_STATE
 - slpublic/SL_GENUINE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Slpublic.h
api_name:
 - SL_GENUINE_STATE
---

# SL_GENUINE_STATE enumeration


## -description

Specifies the state of an application installation.

## -enum-fields

### -field SL_GEN_STATE_IS_GENUINE:0

The installation is genuine.

### -field SL_GEN_STATE_INVALID_LICENSE

The application does not have a valid license.

### -field SL_GEN_STATE_TAMPERED

The <b>Tampered</b> flag of the license associated with the application is set.

### -field SL_GEN_STATE_OFFLINE

The <b>Offline</b> flag of the license associated with the application is set.

### -field SL_GEN_STATE_LAST

The state of the installation has not changed since the last time it was checked.

