---
UID: NE:sessdirpublictypes._TARGET_STATE
title: TARGET_STATE (sessdirpublictypes.h)
description: Indicates the state of a target.
helpviewer_keywords: ["TARGET_CHECKED_OUT","TARGET_DOWN","TARGET_HIBERNATED","TARGET_INITIALIZING","TARGET_RUNNING","TARGET_STATE","TARGET_STATE enumeration [Remote Desktop Services]","TARGET_STOPPED","TARGET_UNKNOWN","sessdirpublictypes/TARGET_CHECKED_OUT","sessdirpublictypes/TARGET_DOWN","sessdirpublictypes/TARGET_HIBERNATED","sessdirpublictypes/TARGET_INITIALIZING","sessdirpublictypes/TARGET_RUNNING","sessdirpublictypes/TARGET_STATE","sessdirpublictypes/TARGET_STOPPED","sessdirpublictypes/TARGET_UNKNOWN","termserv.target_state"]
old-location: termserv\target_state.htm
tech.root: TermServ
ms.assetid: 52ef4bb9-d025-4b54-ac5b-16fa28047cc6
ms.date: 12/05/2018
ms.keywords: TARGET_CHECKED_OUT, TARGET_DOWN, TARGET_HIBERNATED, TARGET_INITIALIZING, TARGET_RUNNING, TARGET_STATE, TARGET_STATE enumeration [Remote Desktop Services], TARGET_STOPPED, TARGET_UNKNOWN, sessdirpublictypes/TARGET_CHECKED_OUT, sessdirpublictypes/TARGET_DOWN, sessdirpublictypes/TARGET_HIBERNATED, sessdirpublictypes/TARGET_INITIALIZING, sessdirpublictypes/TARGET_RUNNING, sessdirpublictypes/TARGET_STATE, sessdirpublictypes/TARGET_STOPPED, sessdirpublictypes/TARGET_UNKNOWN, termserv.target_state
req.header: sessdirpublictypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SessDirPublicTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TARGET_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TARGET_STATE
 - sessdirpublictypes/_TARGET_STATE
 - TARGET_STATE
 - sessdirpublictypes/TARGET_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SessDirPublicTypes.h
api_name:
 - TARGET_STATE
---

# TARGET_STATE enumeration


## -description

Indicates the state of a target.

## -enum-fields

### -field TARGET_UNKNOWN:0x1

The target state is unknown.

### -field TARGET_INITIALIZING

The target is initializing.

### -field TARGET_RUNNING

The target is running.

### -field TARGET_DOWN

The target is not running. If a resource plug-in calls <b>OnStateChange</b> and the target is in this state, RD Connection Broker will delete the target object from its database.

### -field TARGET_HIBERNATED

The target is hibernated.

### -field TARGET_CHECKED_OUT

The target is checked out.

### -field TARGET_STOPPED

The target is stopped.

### -field TARGET_INVALID

### -field TARGET_STARTING

### -field TARGET_STOPPING

### -field TARGET_MAXSTATE

## -see-also

<a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Remote Desktop Virtualization API reference</a>



<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate">SetTargetState</a>



<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate">TargetState</a>
