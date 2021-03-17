---
UID: NS:restartmanager._RM_FILTER_INFO
title: RM_FILTER_INFO (restartmanager.h)
description: Contains information about modifications to restart or shutdown actions.
helpviewer_keywords: ["*PRM_FILTER_INFO","PRM_FILTER_INFO","PRM_FILTER_INFO structure pointer [Restart Mgr]","RM_FILTER_INFO","RM_FILTER_INFO structure [Restart Mgr]","restartmanager/PRM_FILTER_INFO","restartmanager/RM_FILTER_INFO","rstmgr.rm_filter_info"]
old-location: rstmgr\rm_filter_info.htm
tech.root: rstmgr
ms.assetid: b0fd12e4-20e3-48d1-a2db-c1e0334ed427
ms.date: 12/05/2018
ms.keywords: '*PRM_FILTER_INFO, PRM_FILTER_INFO, PRM_FILTER_INFO structure pointer [Restart Mgr], RM_FILTER_INFO, RM_FILTER_INFO structure [Restart Mgr], restartmanager/PRM_FILTER_INFO, restartmanager/RM_FILTER_INFO, rstmgr.rm_filter_info'
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
req.typenames: RM_FILTER_INFO, *PRM_FILTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RM_FILTER_INFO
 - restartmanager/_RM_FILTER_INFO
 - PRM_FILTER_INFO
 - restartmanager/PRM_FILTER_INFO
 - RM_FILTER_INFO
 - restartmanager/RM_FILTER_INFO
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
 - RM_FILTER_INFO
---

# RM_FILTER_INFO structure


## -description

Contains information about modifications to restart or shutdown actions. Add, remove, and list modifications to specified applications and services that have been registered with the Restart Manager session by using the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmaddfilter">RmAddFilter</a>, <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmremovefilter">RmRemoveFilter</a>, and the <a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetfilterlist">RmGetFilterList</a> functions.

## -struct-fields

### -field FilterAction

This member contains a <a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_filter_action">RM_FILTER_ACTION</a> enumeration value. Use the value  <b>RmNoRestart</b> 
to prevent the restart of the application or service. Use the value  <b>RmNoShutdown</b> to prevent the shutdown and restart of the application or service.

### -field FilterTrigger

This member contains a <a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_filter_trigger">RM_FILTER_TRIGGER</a> enumeration value. Use the value  <b>RmFilterTriggerFile</b> to modify the restart or shutdown actions  of an application referenced by the executable's full path filename. Use  the value <b>RmFilterTriggerProcess</b> to modify the restart or shutdown actions   of an application referenced by a <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_unique_process">RM_UNIQUE_PROCESS</a> structure. Use  the value <b>RmFilterTriggerService</b> 
to modify the restart or shutdown actions of a service referenced by the short service name.

### -field cbNextOffset

The offset in bytes to the next structure.

### -field strFilename

If the value of <b>FilterTrigger</b> is <b>RmFilterTriggerFile</b>, this member contains a pointer to a string value that contains the application filename.

### -field Process

If the value of <b>FilterTrigger</b> is  <b>RmFilterTriggerProcess</b>,  this member is a  <a href="/windows/desktop/api/restartmanager/ns-restartmanager-rm_process_info">RM_PROCESS_INFO</a> structure for the application.

### -field strServiceShortName

If the value of <b>FilterTrigger</b> is <b>RmFilterTriggerService</b> this member is a pointer to a string value that contains the short service name.

## -see-also

<a href="/windows/desktop/api/restartmanager/ne-restartmanager-rm_filter_trigger">RM_FILTER_TRIGGER</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmgetfilterlist">RmGetFilterList</a>