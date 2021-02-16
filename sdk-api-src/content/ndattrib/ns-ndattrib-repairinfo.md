---
UID: NS:ndattrib.tagRepairInfo
title: RepairInfo (ndattrib.h)
description: The RepairInfo structure contains data required for a particular repair option.
helpviewer_keywords: ["*PRepairInfo","PRepairInfo","PRepairInfo structure pointer [NDF]","RF_CONTACT_ADMIN","RF_INFORMATION_ONLY","RF_REPRO","RF_RESERVED","RF_RESERVED_CA","RF_RESERVED_LNI","RF_USER_ACTION","RF_USER_CONFIRMATION","RF_VALIDATE_HELPTOPIC","RF_WORKAROUND","RepairInfo","RepairInfo structure [NDF]","ndattrib/PRepairInfo","ndattrib/RepairInfo","ndf.repairinfo"]
old-location: ndf\repairinfo.htm
tech.root: NDF
ms.assetid: 07639ac5-e586-4ab1-96e8-502c378de940
ms.date: 12/05/2018
ms.keywords: '*PRepairInfo, PRepairInfo, PRepairInfo structure pointer [NDF], RF_CONTACT_ADMIN, RF_INFORMATION_ONLY, RF_REPRO, RF_RESERVED, RF_RESERVED_CA, RF_RESERVED_LNI, RF_USER_ACTION, RF_USER_CONFIRMATION, RF_VALIDATE_HELPTOPIC, RF_WORKAROUND, RepairInfo, RepairInfo structure [NDF], ndattrib/PRepairInfo, ndattrib/RepairInfo, ndf.repairinfo'
req.header: ndattrib.h
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
req.typenames: RepairInfo, *PRepairInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRepairInfo
 - ndattrib/tagRepairInfo
 - PRepairInfo
 - ndattrib/PRepairInfo
 - RepairInfo
 - ndattrib/RepairInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - RepairInfo
---

# RepairInfo structure


## -description

The <b>RepairInfo</b> structure contains data required for a particular repair option.

## -struct-fields

### -field guid

A unique GUID for this repair.

### -field pwszClassName

A pointer to a null-terminated  string that contains the helper class name in a user-friendly way.

### -field pwszDescription

A pointer to a null-terminated string that describes the repair in a user friendly way.

### -field sidType

One of the WELL_KNOWN_SID_TYPE if the repair requires certain user contexts or privileges.

### -field cost

The number of seconds required to perform the repair.

### -field flags

Additional information about the repair.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RF_WORKAROUND"></a><a id="rf_workaround"></a><dl>
<dt><b>RF_WORKAROUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the repair is a workaround for the issue.  For example, sometimes resetting a network interface solves intermittent problems, but does not directly address a specific issue, so it is considered a workaround.  NDF will show non-workarounds to the user before workarounds.

</td>
</tr>
<tr>
<td width="40%"><a id="RF_USER_ACTION"></a><a id="rf_user_action"></a><dl>
<dt><b>RF_USER_ACTION</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the repair prompts the user to perform a manual task outside of NDF.

</td>
</tr>
<tr>
<td width="40%"><a id="RF_USER_CONFIRMATION"></a><a id="rf_user_confirmation"></a><dl>
<dt><b>RF_USER_CONFIRMATION</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the repair should not be automatically performed.  The user is instead prompted to select the repair.

</td>
</tr>
<tr>
<td width="40%"><a id="RF_INFORMATION_ONLY"></a><a id="rf_information_only"></a><dl>
<dt><b>RF_INFORMATION_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the repair consists of actionable information for the user.  Repair and validation sessions do not occur for information-only repairs.

</td>
</tr>
<tr>
<td width="40%"><a id="RF_VALIDATE_HELPTOPIC"></a><a id="rf_validate_helptopic"></a><dl>
<dt><b>RF_VALIDATE_HELPTOPIC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the repair provides information to the user as well as a help topic. Unlike <b>RF_INFORMATION_ONLY</b> repairs, which cannot be validated, this repair can be executed and validated within a diagnostic session.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RF_REPRO"></a><a id="rf_repro"></a><dl>
<dt><b>RF_REPRO</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the repair prompts the user to reproduce their problem. At the same time, the helper class may have enabled more detailed logging or other background mechanisms to help detect the failure.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RF_CONTACT_ADMIN"></a><a id="rf_contact_admin"></a><dl>
<dt><b>RF_CONTACT_ADMIN</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the repair prompts the user to contact their network administrator in order to resolve the problem.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RF_RESERVED"></a><a id="rf_reserved"></a><dl>
<dt><b>RF_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
Reserved for system use.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RF_RESERVED_CA"></a><a id="rf_reserved_ca"></a><dl>
<dt><b>RF_RESERVED_CA</b></dt>
</dl>
</td>
<td width="60%">
Reserved for system use.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RF_RESERVED_LNI"></a><a id="rf_reserved_lni"></a><dl>
<dt><b>RF_RESERVED_LNI</b></dt>
</dl>
</td>
<td width="60%">
Reserved for system use.

<div class="alert"><b>Note</b>  Available only in Windows 7, Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
</table>

### -field scope

Reserved for future use.

### -field risk

Reserved for future use.

### -field UiInfo

A <a href="/windows/desktop/api/ndattrib/ns-ndattrib-uiinfo">UiInfo</a> structure.

### -field rootCauseIndex

## -see-also

<a href="/windows/desktop/NDF/copyrepairinfo">CopyRepairInfo</a>



<a href="/windows/desktop/NDF/freerepairinfos">FreeRepairInfos</a>



<a href="/windows/desktop/api/ndattrib/ns-ndattrib-uiinfo">UiInfo</a>