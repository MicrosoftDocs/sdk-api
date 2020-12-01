---
UID: NE:sessdirpublictypes._TARGET_CHANGE_TYPE
title: TARGET_CHANGE_TYPE (sessdirpublictypes.h)
description: Specifies the type of change that occurred in a target.
helpviewer_keywords: ["TARGET_CHANGE_TYPE","TARGET_CHANGE_TYPE enumeration [Remote Desktop Services]","TARGET_CHANGE_UNSPEC","TARGET_EXTERNALIP_CHANGED","TARGET_IDLE","TARGET_INTERNALIP_CHANGED","TARGET_JOINED","TARGET_REMOVED","TARGET_STATE_CHANGED","sessdirpublictypes/TARGET_CHANGE_TYPE","sessdirpublictypes/TARGET_CHANGE_UNSPEC","sessdirpublictypes/TARGET_EXTERNALIP_CHANGED","sessdirpublictypes/TARGET_IDLE","sessdirpublictypes/TARGET_INTERNALIP_CHANGED","sessdirpublictypes/TARGET_JOINED","sessdirpublictypes/TARGET_REMOVED","sessdirpublictypes/TARGET_STATE_CHANGED","termserv.target_change_type"]
old-location: termserv\target_change_type.htm
tech.root: TermServ
ms.assetid: ee1e6433-498f-4d8a-97d7-3e32f79fafda
ms.date: 12/05/2018
ms.keywords: TARGET_CHANGE_TYPE, TARGET_CHANGE_TYPE enumeration [Remote Desktop Services], TARGET_CHANGE_UNSPEC, TARGET_EXTERNALIP_CHANGED, TARGET_IDLE, TARGET_INTERNALIP_CHANGED, TARGET_JOINED, TARGET_REMOVED, TARGET_STATE_CHANGED, sessdirpublictypes/TARGET_CHANGE_TYPE, sessdirpublictypes/TARGET_CHANGE_UNSPEC, sessdirpublictypes/TARGET_EXTERNALIP_CHANGED, sessdirpublictypes/TARGET_IDLE, sessdirpublictypes/TARGET_INTERNALIP_CHANGED, sessdirpublictypes/TARGET_JOINED, sessdirpublictypes/TARGET_REMOVED, sessdirpublictypes/TARGET_STATE_CHANGED, termserv.target_change_type
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
req.typenames: TARGET_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TARGET_CHANGE_TYPE
 - sessdirpublictypes/_TARGET_CHANGE_TYPE
 - TARGET_CHANGE_TYPE
 - sessdirpublictypes/TARGET_CHANGE_TYPE
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
 - TARGET_CHANGE_TYPE
---

# TARGET_CHANGE_TYPE enumeration


## -description

Specifies the type of change that occurred in a target.

## -enum-fields

### -field TARGET_CHANGE_UNSPEC

Unspecified change in the target.

### -field TARGET_EXTERNALIP_CHANGED

The target's external IP address changed.

### -field TARGET_INTERNALIP_CHANGED

The target's internal IP address changed.

### -field TARGET_JOINED

The target was reported to RD Connection Broker.

### -field TARGET_REMOVED

The target was deleted  from the store in RD Connection Broker.

### -field TARGET_STATE_CHANGED

The target's state changed. To determine the current state of the target, check the <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate">TargetState</a> property of <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>.

### -field TARGET_IDLE

The target is not hosting any sessions currently.

### -field TARGET_PENDING

### -field TARGET_INUSE

### -field TARGET_PATCH_STATE_CHANGED

### -field TARGET_FARM_MEMBERSHIP_CHANGED

## -see-also

<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcenotification-notifytargetchange">NotifyTargetChange</a>



<a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Remote Desktop Virtualization API reference</a>