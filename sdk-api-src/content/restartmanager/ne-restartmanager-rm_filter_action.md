---
UID: NE:restartmanager._RM_FILTER_ACTION
title: RM_FILTER_ACTION (restartmanager.h)
description: Specifies the type of modification that is applied to restart or shutdown actions.
helpviewer_keywords: ["RM_FILTER_ACTION","RM_FILTER_ACTION enumeration [Restart Mgr]","RmInvalidFilterAction","RmNoRestart","RmNoShutdown","restartmanager/RM_FILTER_ACTION","restartmanager/RmInvalidFilterAction","restartmanager/RmNoRestart","restartmanager/RmNoShutdown","rstmgr.rm_filter_action"]
old-location: rstmgr\rm_filter_action.htm
tech.root: rstmgr
ms.assetid: 68f77dbc-14cb-4b87-9589-328b1cef38d9
ms.date: 12/05/2018
ms.keywords: RM_FILTER_ACTION, RM_FILTER_ACTION enumeration [Restart Mgr], RmInvalidFilterAction, RmNoRestart, RmNoShutdown, restartmanager/RM_FILTER_ACTION, restartmanager/RmInvalidFilterAction, restartmanager/RmNoRestart, restartmanager/RmNoShutdown, rstmgr.rm_filter_action
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
req.typenames: RM_FILTER_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_FILTER_ACTION
 - restartmanager/_RM_FILTER_ACTION
 - RM_FILTER_ACTION
 - restartmanager/RM_FILTER_ACTION
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
 - RM_FILTER_ACTION
---

# RM_FILTER_ACTION enumeration


## -description

Specifies the type of modification that is applied to restart or shutdown actions.

## -enum-fields

### -field RmInvalidFilterAction:0

An invalid filter action.

### -field RmNoRestart:1

Prevents the restart of the specified application or service.

### -field RmNoShutdown

Prevents the shut down and restart of the specified application or service.

## -see-also

<a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_filter_info">RM_FILTER_INFO</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a>
