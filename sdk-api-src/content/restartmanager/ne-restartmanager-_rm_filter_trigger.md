---
UID: NE:restartmanager._RM_FILTER_TRIGGER
title: "_RM_FILTER_TRIGGER"
author: windows-sdk-content
description: Describes the restart or shutdown actions for an application or service.
old-location: rstmgr\rm_filter_trigger.htm
old-project: RstMgr
ms.assetid: 1198c52b-f5f5-46e9-878e-39143687d645
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RM_FILTER_TRIGGER, RM_FILTER_TRIGGER enumeration [Restart Mgr], RmFilterTriggerFile, RmFilterTriggerInvalid, RmFilterTriggerProcess, RmFilterTriggerService, _RM_FILTER_TRIGGER, restartmanager/RM_FILTER_TRIGGER, restartmanager/RmFilterTriggerFile, restartmanager/RmFilterTriggerInvalid, restartmanager/RmFilterTriggerProcess, restartmanager/RmFilterTriggerService, rstmgr.rm_filter_trigger
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: RM_FILTER_TRIGGER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	RestartManager.h
api_name:
-	RM_FILTER_TRIGGER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _RM_FILTER_TRIGGER enumeration


## -description


Describes the restart or shutdown actions for an application or service.


## -enum-fields




### -field RmFilterTriggerInvalid

An invalid filter trigger.


### -field RmFilterTriggerFile

Modifies the shutdown or restart actions for an application identified by its   executable filename.


### -field RmFilterTriggerProcess

Modifies the shutdown or restart actions for an application identified by a <a href="https://msdn.microsoft.com/5e3698c7-1ea8-4f9d-8fae-e69055a000fc">RM_UNIQUE_PROCESS</a> structure.


### -field RmFilterTriggerService

Modifies the shutdown or restart actions for a service identified by a service short name.


## -see-also




<a href="https://msdn.microsoft.com/b0fd12e4-20e3-48d1-a2db-c1e0334ed427">RM_FILTER_INFO</a>
 

 

