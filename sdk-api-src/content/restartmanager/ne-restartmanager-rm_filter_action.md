---
UID: NE:restartmanager._RM_FILTER_ACTION
title: RM_FILTER_ACTION
author: windows-sdk-content
description: Specifies the type of modification that is applied to restart or shutdown actions.
old-location: rstmgr\rm_filter_action.htm
tech.root: rstmgr
ms.assetid: 68f77dbc-14cb-4b87-9589-328b1cef38d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RM_FILTER_ACTION, RM_FILTER_ACTION enumeration [Restart Mgr], RmInvalidFilterAction, RmNoRestart, RmNoShutdown, restartmanager/RM_FILTER_ACTION, restartmanager/RmInvalidFilterAction, restartmanager/RmNoRestart, restartmanager/RmNoShutdown, rstmgr.rm_filter_action
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RestartManager.h
api_name:
 - RM_FILTER_ACTION
product: Windows
targetos: Windows
req.typenames: RM_FILTER_ACTION
req.redist: 
---

# RM_FILTER_ACTION enumeration


## -description


Specifies the type of modification that is applied to restart or shutdown actions.


## -enum-fields




### -field RmInvalidFilterAction

An invalid filter action.


### -field RmNoRestart

Prevents the restart of the specified application or service.


### -field RmNoShutdown

Prevents the shut down and restart of the specified application or service.




## -see-also




<a href="https://msdn.microsoft.com/b0fd12e4-20e3-48d1-a2db-c1e0334ed427">RM_FILTER_INFO</a>



<a href="https://msdn.microsoft.com/63d1d1d2-d7b7-4d6c-99f9-b849229e171f">RmAddFilter</a>
 

 

