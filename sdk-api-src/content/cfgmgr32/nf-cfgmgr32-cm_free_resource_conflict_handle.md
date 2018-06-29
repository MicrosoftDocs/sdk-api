---
UID: NF:cfgmgr32.CM_Free_Resource_Conflict_Handle
title: CM_Free_Resource_Conflict_Handle function
author: windows-sdk-content
description: The CM_Free_Resource_Conflict_Handle function invalidates a handle to a resource conflict list, and frees the handle's associated memory allocation.
old-location: devinst\cm_free_resource_conflict_handle.htm
old-project: devinst
ms.assetid: 8c6b4f0d-d4d0-44dc-9a8f-5e3fe36c73a5
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CM_Free_Resource_Conflict_Handle, CM_Free_Resource_Conflict_Handle function [Device and Driver Installation], cfgmgr32/CM_Free_Resource_Conflict_Handle, cfgmgrfn_e6d2dc8a-4aa5-4271-808f-f16a885f9ad2.xml, devinst.cm_free_resource_conflict_handle
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
 - CM_Free_Resource_Conflict_Handle
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Free_Resource_Conflict_Handle function


## -description


The <b>CM_Free_Resource_Conflict_Handle</b> function invalidates a handle to a resource conflict list, and frees the handle's associated memory allocation.


## -parameters




### -param clConflictList [in]

Caller-supplied handle to be freed. This conflict list handle must have been previously obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff539760">CM_Query_Resource_Conflict_List</a>.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



An application must call <b>CM_Free_Resource_Conflict_Handle</b> after it has finished using the handle that was obtained calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff539760">CM_Query_Resource_Conflict_List</a>.



