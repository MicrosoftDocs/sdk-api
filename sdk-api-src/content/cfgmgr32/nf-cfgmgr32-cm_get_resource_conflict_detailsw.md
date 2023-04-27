---
UID: NF:cfgmgr32.CM_Get_Resource_Conflict_DetailsW
title: CM_Get_Resource_Conflict_DetailsW function (cfgmgr32.h)
description: The CM_Get_Resource_Conflict_Details function obtains the details about one of the resource conflicts in a conflict list. (Unicode)
helpviewer_keywords: ["CM_Get_Resource_Conflict_Details", "CM_Get_Resource_Conflict_Details function [Device and Driver Installation]", "CM_Get_Resource_Conflict_DetailsW", "cfgmgr32/CM_Get_Resource_Conflict_Details", "cfgmgr32/CM_Get_Resource_Conflict_DetailsW", "cfgmgrfn_c646fbb1-7baa-4429-b3c6-02e2aced8ddc.xml", "devinst.cm_get_resource_conflict_details"]
old-location: devinst\cm_get_resource_conflict_details.htm
tech.root: devinst
ms.assetid: ce4691e2-4a0e-48bf-b085-ac0cb7665725
ms.date: 12/05/2018
ms.keywords: CM_Get_Resource_Conflict_Details, CM_Get_Resource_Conflict_Details function [Device and Driver Installation], CM_Get_Resource_Conflict_DetailsW, cfgmgr32/CM_Get_Resource_Conflict_Details, cfgmgr32/CM_Get_Resource_Conflict_DetailsW, cfgmgrfn_c646fbb1-7baa-4429-b3c6-02e2aced8ddc.xml, devinst.cm_get_resource_conflict_details
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Resource_Conflict_DetailsW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Resource_Conflict_DetailsW
 - cfgmgr32/CM_Get_Resource_Conflict_DetailsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Cfgmgr32.lib
 - Cfgmgr32.dll
api_name:
 - CM_Get_Resource_Conflict_Details
 - CM_Get_Resource_Conflict_DetailsW
---

# CM_Get_Resource_Conflict_DetailsW function


## -description

The <b>CM_Get_Resource_Conflict_Details</b> function obtains the details about one of the resource conflicts in a conflict list.

## -parameters

### -param clConflictList [in]

Caller-supplied handle to a conflict list, obtained by a previous call to <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list">CM_Query_Resource_Conflict_List</a>.

### -param ulIndex [in]

Caller-supplied value used as an index into the conflict list. This value can be from zero to one less than the number returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count">CM_Get_Resource_Conflict_Count</a>.

### -param pConflictDetails [in, out]

Caller-supplied address of a <a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a">CONFLICT_DETAILS</a> structure to receive conflict details. The caller must supply values for the structure's <i>CD_ulSize</i> and <i>CD_ulMask</i> structures.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

To determine conflicting resource requirements between a specified device and other devices on a machine, use the following steps.

<ol>
<li>
Call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list">CM_Query_Resource_Conflict_List</a> to obtain a handle to a list of resource conflicts.

</li>
<li>
Call <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count">CM_Get_Resource_Conflict_Count</a> to determine the number of conflicts contained in the resource conflict list.

</li>
<li>
Call <b>CM_Get_Resource_Conflict_Details</b> for each entry in the conflict list.

</li>
</ol>
The following conflicts are typically not reported:

<ul>
<li>
If there are multiple conflicts for a resource, and the owners of only some of the conflicts can be determined, the conflicts without identifiable owners are not reported.

</li>
<li>
Conflicts that appear to be with the specified device (that is, the device conflicts with itself) are not reported.

</li>
<li>
If multiple non-Plug and Play devices use the same driver, resource conflicts among these devices might not be reported.

</li>
</ul>
Sometimes, resources assigned to the HAL might be reported as either conflicting with the HAL or not available.
