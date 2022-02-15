---
UID: NE:restartmanager._RM_FILTER_TRIGGER
title: RM_FILTER_TRIGGER (restartmanager.h)
description: Describes the restart or shutdown actions for an application or service.
helpviewer_keywords: ["RM_FILTER_TRIGGER","RM_FILTER_TRIGGER enumeration [Restart Mgr]","RmFilterTriggerFile","RmFilterTriggerInvalid","RmFilterTriggerProcess","RmFilterTriggerService","restartmanager/RM_FILTER_TRIGGER","restartmanager/RmFilterTriggerFile","restartmanager/RmFilterTriggerInvalid","restartmanager/RmFilterTriggerProcess","restartmanager/RmFilterTriggerService","rstmgr.rm_filter_trigger"]
old-location: rstmgr\rm_filter_trigger.htm
tech.root: rstmgr
ms.assetid: 1198c52b-f5f5-46e9-878e-39143687d645
ms.date: 12/05/2018
ms.keywords: RM_FILTER_TRIGGER, RM_FILTER_TRIGGER enumeration [Restart Mgr], RmFilterTriggerFile, RmFilterTriggerInvalid, RmFilterTriggerProcess, RmFilterTriggerService, restartmanager/RM_FILTER_TRIGGER, restartmanager/RmFilterTriggerFile, restartmanager/RmFilterTriggerInvalid, restartmanager/RmFilterTriggerProcess, restartmanager/RmFilterTriggerService, rstmgr.rm_filter_trigger
req.header: restartmanager.h
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
req.typenames: RM_FILTER_TRIGGER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_FILTER_TRIGGER
 - restartmanager/_RM_FILTER_TRIGGER
 - RM_FILTER_TRIGGER
 - restartmanager/RM_FILTER_TRIGGER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RestartManager.h
api_name:
 - RM_FILTER_TRIGGER
---

# RM_FILTER_TRIGGER enumeration


## -description

Describes the restart or shutdown actions for an application or service.

## -enum-fields

### -field RmFilterTriggerInvalid:0

An invalid filter trigger.

### -field RmFilterTriggerFile

Modifies the shutdown or restart actions for an application identified by its   executable filename.

### -field RmFilterTriggerProcess

Modifies the shutdown or restart actions for an application identified by a <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_unique_process">RM_UNIQUE_PROCESS</a> structure.

### -field RmFilterTriggerService

Modifies the shutdown or restart actions for a service identified by a service short name.

## -see-also

<a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_filter_info">RM_FILTER_INFO</a>
