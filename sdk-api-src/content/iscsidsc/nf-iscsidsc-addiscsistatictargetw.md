---
UID: NF:iscsidsc.AddIScsiStaticTargetW
title: AddIScsiStaticTargetW function (iscsidsc.h)
description: AddIscsiStaticTarget function adds a target to the list of static targets available to the iSCSI initiator. (Unicode)
helpviewer_keywords: ["AddIScsiStaticTargetW", "AddIscsiStaticTarget", "AddIscsiStaticTarget function [iSCSI Discovery Library API]", "AddIscsiStaticTargetW", "ISCSI_TARGET_FLAG_HIDE_STATIC_TARGET", "ISCSI_TARGET_FLAG_MERGE_TARGET_INFORMATION", "iscsidisc.addiscsistatictarget", "iscsidsc/AddIscsiStaticTarget", "iscsidsc/AddIscsiStaticTargetW"]
old-location: iscsidisc\addiscsistatictarget.htm
tech.root: iSCSIDisc
ms.assetid: 81f5ac9a-debb-4fa3-8ccf-1303cd45f1de
ms.date: 12/05/2018
ms.keywords: AddIScsiStaticTargetW, AddIscsiStaticTarget, AddIscsiStaticTarget function [iSCSI Discovery Library API], AddIscsiStaticTargetA, AddIscsiStaticTargetW, ISCSI_TARGET_FLAG_HIDE_STATIC_TARGET, ISCSI_TARGET_FLAG_MERGE_TARGET_INFORMATION, iscsidisc.addiscsistatictarget, iscsidsc/AddIscsiStaticTarget, iscsidsc/AddIscsiStaticTargetA, iscsidsc/AddIscsiStaticTargetW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddIscsiStaticTargetW (Unicode) and AddIscsiStaticTargetA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddIScsiStaticTargetW
 - iscsidsc/AddIScsiStaticTargetW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - AddIscsiStaticTarget
 - AddIscsiStaticTargetA
 - AddIscsiStaticTargetW
---

# AddIScsiStaticTargetW function


## -description

The <b>AddIscsiStaticTarget</b> function adds a target to the list of static targets available to the iSCSI initiator.

## -parameters

### -param TargetName [in]

The name of the target to add to the static target list.

### -param TargetAlias [in, optional]

An alias associated with the <i>TargetName</i>.

### -param TargetFlags [in]

A bitmap of flags that affect how, and under what circumstances, a target is discovered and enumerated. 

The following table lists the flags that can be associated with a target and the meaning of each flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISCSI_TARGET_FLAG_HIDE_STATIC_TARGET"></a><a id="iscsi_target_flag_hide_static_target"></a><dl>
<dt><b>ISCSI_TARGET_FLAG_HIDE_STATIC_TARGET</b></dt>
</dl>
</td>
<td width="60%">
The target is added to the list of static targets. However, <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsitargetsa">ReportIscsiTargets</a> does not report the target, unless it was also discovered dynamically by the iSCSI initiator, the Internet Storage Name Service (iSNS), or a <b>SendTargets</b> request.

</td>
</tr>
<tr>
<td width="40%"><a id="ISCSI_TARGET_FLAG_MERGE_TARGET_INFORMATION"></a><a id="iscsi_target_flag_merge_target_information"></a><dl>
<dt><b>ISCSI_TARGET_FLAG_MERGE_TARGET_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
The iSCSI initiator service merges the information (if any) that it already has for this static target with the information that the caller passes to <b>AddIscsiStaticTarget</b>. 

If this flag is not set, the iSCSI initiator service overwrites the stored information with the information that the caller passes in.

</td>
</tr>
</table>

### -param Persist [in]

If <b>true</b>, the target information persists across restarts of the iSCSI initiator service.

### -param Mappings [in, optional]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a> that contains a set of mappings that the initiator uses when assigning values for the bus, target, and LUN numbers to the iSCSI LUNs associated with the target. 
If <i>Mappings</i> is <b>null</b>, the initiator will select the bus, target, and LUN numbers.

### -param LoginOptions [in, optional]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a> that contains the options that specify the default login parameters that an initiator uses to login to a target.

### -param PortalGroup [in, optional]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portal_groupa">ISCSI_TARGET_PORTAL_GROUP</a> that indicates the group of portals that an initiator can use login to the target.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -remarks

This routine adds a target to the iSCSI initiator service's list of static targets. If the caller specifies a value of <b>true</b> in <i>Persist</i>, the target is stored in the registry and information about the target persists across restarts of the initiator service and reboots of the operating system.

By setting the <b>ISCSI_TARGET_FLAG_HIDE_STATIC_TARGET</b> flag, callers can configure default login information for a target prior to its discovery by an iSCSI initiator, the iSNS service, or a SendTargets request.





> [!NOTE]
> The iscsidsc.h header defines AddIScsiStaticTarget as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portal_groupa">ISCSI_TARGET_PORTAL_GROUP</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeiscsistatictargeta">RemoveIscsiStaticTarget</a>
