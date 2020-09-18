---
UID: NF:cfgmgr32.CM_Free_Resource_Conflict_Handle
title: CM_Free_Resource_Conflict_Handle function (cfgmgr32.h)
description: The CM_Free_Resource_Conflict_Handle function invalidates a handle to a resource conflict list, and frees the handle's associated memory allocation.
helpviewer_keywords: ["CM_Free_Resource_Conflict_Handle","CM_Free_Resource_Conflict_Handle function [Device and Driver Installation]","cfgmgr32/CM_Free_Resource_Conflict_Handle","cfgmgrfn_e6d2dc8a-4aa5-4271-808f-f16a885f9ad2.xml","devinst.cm_free_resource_conflict_handle"]
old-location: devinst\cm_free_resource_conflict_handle.htm
tech.root: devinst
ms.assetid: 8c6b4f0d-d4d0-44dc-9a8f-5e3fe36c73a5
ms.date: 12/05/2018
ms.keywords: CM_Free_Resource_Conflict_Handle, CM_Free_Resource_Conflict_Handle function [Device and Driver Installation], cfgmgr32/CM_Free_Resource_Conflict_Handle, cfgmgrfn_e6d2dc8a-4aa5-4271-808f-f16a885f9ad2.xml, devinst.cm_free_resource_conflict_handle
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
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Free_Resource_Conflict_Handle
 - cfgmgr32/CM_Free_Resource_Conflict_Handle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Free_Resource_Conflict_Handle
---

# CM_Free_Resource_Conflict_Handle function


## -description

The <b>CM_Free_Resource_Conflict_Handle</b> function invalidates a handle to a resource conflict list, and frees the handle's associated memory allocation.

## -parameters

### -param clConflictList [in]

Caller-supplied handle to be freed. This conflict list handle must have been previously obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list">CM_Query_Resource_Conflict_List</a>.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

An application must call <b>CM_Free_Resource_Conflict_Handle</b> after it has finished using the handle that was obtained calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list">CM_Query_Resource_Conflict_List</a>.