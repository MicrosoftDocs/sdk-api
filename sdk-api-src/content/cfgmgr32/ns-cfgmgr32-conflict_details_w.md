---
UID: NS:cfgmgr32._CONFLICT_DETAILS_W
title: CONFLICT_DETAILS_W (cfgmgr32.h)
description: The CONFLICT_DETAILS structure is used as a parameter to the CM_Get_Resource_Conflict_Details function. (Unicode)
helpviewer_keywords: ["*PCONFLICT_DETAILS_W","CONFLICT_DETAILS","CONFLICT_DETAILS structure [Device and Driver Installation]","CONFLICT_DETAILS_W","PCONFLICT_DETAILS","PCONFLICT_DETAILS structure pointer [Device and Driver Installation]","cfgmgr32/CONFLICT_DETAILS","cfgmgr32/PCONFLICT_DETAILS","cfgmgrst_c9b5c398-f35c-4c09-9e25-8949b1d8dc1a.xml","devinst.conflict_details"]
old-location: devinst\conflict_details.htm
tech.root: devinst
ms.assetid: 7f095104-4478-4047-b411-ac6bcc44a11f
ms.date: 12/05/2018
ms.keywords: '*PCONFLICT_DETAILS_W, CONFLICT_DETAILS, CONFLICT_DETAILS structure [Device and Driver Installation], CONFLICT_DETAILS_W, PCONFLICT_DETAILS, PCONFLICT_DETAILS structure pointer [Device and Driver Installation], cfgmgr32/CONFLICT_DETAILS, cfgmgr32/PCONFLICT_DETAILS, cfgmgrst_c9b5c398-f35c-4c09-9e25-8949b1d8dc1a.xml, devinst.conflict_details'
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CONFLICT_DETAILS_W
 - cfgmgr32/_CONFLICT_DETAILS_W
 - PCONFLICT_DETAILS_W
 - cfgmgr32/PCONFLICT_DETAILS_W
 - CONFLICT_DETAILS_W
 - cfgmgr32/CONFLICT_DETAILS_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - CONFLICT_DETAILS
 - conflict_details_w
---

# CONFLICT_DETAILS_W structure


## -description

The CONFLICT_DETAILS structure is used as a parameter to the <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw">CM_Get_Resource_Conflict_Details</a> function.

## -struct-fields

### -field CD_ulSize

Size, in bytes, of the CONFLICT_DETAILS structure.

### -field CD_ulMask

One or more bit flags supplied by the caller of <b>CM_Get_Resource_Conflict_Details</b>. The bit flags are described in the following table.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>
CM_CDMASK_DEVINST

</td>
<td>
If set, <b>CM_Get_Resource_Conflict_Details</b> supplies a value for the <b>CD_dnDevInst</b> member.

</td>
</tr>
<tr>
<td>
CM_CDMASK_RESDES

</td>
<td>
<i>Not used.</i>

</td>
</tr>
<tr>
<td>
CM_CDMASK_FLAGS

</td>
<td>
If set, <b>CM_Get_Resource_Conflict_Details</b> supplies a value for the <b>CD_ulFlags</b> member.

</td>
</tr>
<tr>
<td>
CM_CDMASK_DESCRIPTION

</td>
<td>
If set, <b>CM_Get_Resource_Conflict_Details</b> supplies a value for the <b>CD_szDescription</b> member.

</td>
</tr>
</table>

### -field CD_dnDevInst

If CM_CDMASK_DEVINST is set in <b>CD_ulMask</b>, this member will receive a handle to a device instance that has conflicting resources. If a handle is not obtainable, the member receives -1.

### -field CD_rdResDes

<i>Not used.</i>

### -field CD_ulFlags

If CM_CDMASK_FLAGS is set in <b>CD_ulMask</b>, this member can receive bit flags listed in the following table.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>
CM_CDFLAGS_DRIVER

</td>
<td>
If set, the string contained in the <b>CD_szDescription</b> member represents a driver name instead of a device name, and <b>CD_dnDevInst</b> is -1.

</td>
</tr>
<tr>
<td>
CM_CDFLAGS_ROOT_OWNED

</td>
<td>
If set, the conflicting resources are owned by the root device (that is, the HAL), and <b>CD_dnDevInst</b> is -1.

</td>
</tr>
<tr>
<td>
CM_CDFLAGS_RESERVED

</td>
<td>
If set, the owner of the conflicting resources cannot be determined, and <b>CD_dnDevInst</b> is -1.

</td>
</tr>
</table>

### -field CD_szDescription

If CM_CDMASK_DESCRIPTION is set in <b>CD_ulMask</b>, this member will receive a NULL-terminated text string representing a description of the device that owns the resources. If CM_CDFLAGS_DRIVER is set in <b>CD_ulFlags</b>, this string represents a driver name. If CM_CDFLAGS_ROOT_OWNED or CM_CDFLAGS_RESERVED is set, the string value is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw">CM_Get_Resource_Conflict_Details</a>

## -remarks

> [!NOTE]
> The cfgmgr32.h header defines CONFLICT_DETAILS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
