---
UID: NS:restartmanager._RM_FILTER_INFO
title: "_RM_FILTER_INFO"
author: windows-driver-content
description: Contains information about modifications to restart or shutdown actions.
old-location: rstmgr\rm_filter_info.htm
old-project: RstMgr
ms.assetid: b0fd12e4-20e3-48d1-a2db-c1e0334ed427
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PRM_FILTER_INFO, PRM_FILTER_INFO, PRM_FILTER_INFO structure pointer [Restart Mgr], RM_FILTER_INFO, RM_FILTER_INFO structure [Restart Mgr], _RM_FILTER_INFO, restartmanager/PRM_FILTER_INFO, restartmanager/RM_FILTER_INFO, rstmgr.rm_filter_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: RM_FILTER_INFO, *PRM_FILTER_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	RestartManager.h
api_name:
-	RM_FILTER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _RM_FILTER_INFO structure


## -description


Contains information about modifications to restart or shutdown actions. Add, remove, and list modifications to specified applications and services that have been registered with the Restart Manager session by using the <a href="https://msdn.microsoft.com/63d1d1d2-d7b7-4d6c-99f9-b849229e171f">RmAddFilter</a>, <a href="https://msdn.microsoft.com/fb1baa7b-0dfb-4bd1-8a3f-cfaf9bf4079f">RmRemoveFilter</a>, and the <a href="https://msdn.microsoft.com/61427838-8b23-4105-93fd-55f457fd43a7">RmGetFilterList</a> functions.


## -struct-fields




### -field FilterAction

This member contains a <a href="https://msdn.microsoft.com/68f77dbc-14cb-4b87-9589-328b1cef38d9">RM_FILTER_ACTION</a> enumeration value. Use the value  <b>RmNoRestart</b> 
to prevent the restart of the application or service. Use the value  <b>RmNoShutdown</b> to prevent the shutdown and restart of the application or service.


### -field FilterTrigger

This member contains a <a href="https://msdn.microsoft.com/1198c52b-f5f5-46e9-878e-39143687d645">RM_FILTER_TRIGGER</a> enumeration value. Use the value  <b>RmFilterTriggerFile</b> to modify the restart or shutdown actions  of an application referenced by the executable's full path filename. Use  the value <b>RmFilterTriggerProcess</b> to modify the restart or shutdown actions   of an application referenced by a <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structure. Use  the value <b>RmFilterTriggerService</b> 
to modify the restart or shutdown actions of a service referenced by the short service name.


### -field cbNextOffset

The offset in bytes to the next structure.


#### - Process

If the value of <b>FilterTrigger</b> is  <b>RmFilterTriggerProcess</b>,  this member is a  <a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a> structure for the application.


#### - strFilename

If the value of <b>FilterTrigger</b> is <b>RmFilterTriggerFile</b>, this member contains a pointer to a string value that contains the application filename.


#### - strServiceShortName

If the value of <b>FilterTrigger</b> is <b>RmFilterTriggerService</b> this member is a pointer to a string value that contains the short service name.


## -see-also




<a href="https://msdn.microsoft.com/1198c52b-f5f5-46e9-878e-39143687d645">RM_FILTER_TRIGGER</a>



<a href="https://msdn.microsoft.com/61427838-8b23-4105-93fd-55f457fd43a7">RmGetFilterList</a>
 

 

