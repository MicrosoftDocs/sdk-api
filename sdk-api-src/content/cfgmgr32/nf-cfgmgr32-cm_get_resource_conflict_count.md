---
UID: NF:cfgmgr32.CM_Get_Resource_Conflict_Count
title: CM_Get_Resource_Conflict_Count function
author: windows-sdk-content
description: The CM_Get_Resource_Conflict_Count function obtains the number of conflicts contained in a specified resource conflict list.
old-location: devinst\cm_get_resource_conflict_count.htm
old-project: devinst
ms.assetid: 758fbc4c-499f-492d-b64d-f80b1fc7ee25
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: CM_Get_Resource_Conflict_Count, CM_Get_Resource_Conflict_Count function [Device and Driver Installation], cfgmgr32/CM_Get_Resource_Conflict_Count, cfgmgrfn_ac18aaca-cd62-4629-a29e-c717b293e8c9.xml, devinst.cm_get_resource_conflict_count
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Get_Resource_Conflict_Count
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Get_Resource_Conflict_Count function


## -description


The <b>CM_Get_Resource_Conflict_Count</b> function obtains the number of conflicts contained in a specified resource conflict list.


## -parameters




### -param clConflictList [in]

Caller-supplied handle to a conflict list, obtained by a previous call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539760">CM_Query_Resource_Conflict_List</a>.


### -param pulCount [out]

Caller-supplied address of a location to receive the conflict count.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



The count value obtained by calling <b>CM_Get_Resource_Conflict_Count</b> can be used to determine the number of times to call <a href="https://msdn.microsoft.com/library/windows/hardware/ff538631">CM_Get_Resource_Conflict_Details</a>, which supplies information about each conflict.

If there are no entries in the conflict list, the location supplied by <i>pulCount</i> will receive zero.



