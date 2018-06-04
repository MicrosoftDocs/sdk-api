---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagRepairInfo structure


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

A <a href="https://msdn.microsoft.com/62d3c908-8fc4-4bd9-94ac-94dfcf8db395">UiInfo</a> structure.


### -field rootCauseIndex

 




## -see-also




<a href="https://msdn.microsoft.com/a1147ce6-9a90-4a46-8fe4-da3353391a13">CopyRepairInfo</a>



<a href="https://msdn.microsoft.com/c40f9d10-8d9e-4c79-ac0b-fa88608888f1">FreeRepairInfos</a>



<a href="https://msdn.microsoft.com/62d3c908-8fc4-4bd9-94ac-94dfcf8db395">UiInfo</a>
 

 

