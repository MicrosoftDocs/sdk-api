---
UID: NE:iscsidsc.TARGET_INFORMATION_CLASS
title: TARGET_INFORMATION_CLASS (iscsidsc.h)
description: TARGET_INFORMATION_CLASS enumeration specifies information about the indicated target device that the GetIScsiTargetInformation function retrieves.
helpviewer_keywords: ["*PTARGET_INFORMATION_CLASS","DiscoveryMechanism","InitiatorName","LoginOptions","PersistentTargetMappings","PortalGroups","ProtocolType","TARGET_INFORMATION_CLASS","TARGET_INFORMATION_CLASS enumeration [iSCSI Discovery Library API]","TargetAlias","TargetFlags","iscsidisc.target_information_class","iscsidsc/DiscoveryMechanism","iscsidsc/InitiatorName","iscsidsc/LoginOptions","iscsidsc/PersistentTargetMappings","iscsidsc/PortalGroups","iscsidsc/ProtocolType","iscsidsc/TARGET_INFORMATION_CLASS","iscsidsc/TargetAlias","iscsidsc/TargetFlags"]
old-location: iscsidisc\target_information_class.htm
tech.root: iSCSIDisc
ms.assetid: 2ef6cff7-b5ab-463d-b274-62be81bc9295
ms.date: 12/05/2018
ms.keywords: '*PTARGET_INFORMATION_CLASS, DiscoveryMechanism, InitiatorName, LoginOptions, PersistentTargetMappings, PortalGroups, ProtocolType, TARGET_INFORMATION_CLASS, TARGET_INFORMATION_CLASS enumeration [iSCSI Discovery Library API], TargetAlias, TargetFlags, iscsidisc.target_information_class, iscsidsc/DiscoveryMechanism, iscsidsc/InitiatorName, iscsidsc/LoginOptions, iscsidsc/PersistentTargetMappings, iscsidsc/PortalGroups, iscsidsc/ProtocolType, iscsidsc/TARGET_INFORMATION_CLASS, iscsidsc/TargetAlias, iscsidsc/TargetFlags'
req.header: iscsidsc.h
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
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTARGET_INFORMATION_CLASS
 - iscsidsc/PTARGET_INFORMATION_CLASS
 - TARGET_INFORMATION_CLASS
 - iscsidsc/TARGET_INFORMATION_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - TARGET_INFORMATION_CLASS
---

## -description

The <b>TARGET_INFORMATION_CLASS</b> enumeration specifies information about the indicated target device that the <a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-getiscsitargetinformationa">GetIScsiTargetInformation</a> function retrieves.

## -enum-fields

### -field ProtocolType

A value of the <a href="/previous-versions/windows/desktop/api/iscsidsc/ne-iscsidsc-targetprotocoltype">TARGETPROTOCOLTYPE</a> structure, indicating the protocol that the initiator uses to communicate with the target device.

### -field TargetAlias

A <b>null</b>-terminated string that contains the alias of the target device.

### -field DiscoveryMechanisms

A list of <b>null</b>-terminated strings that describe the discovery mechanisms that located the indicated target. The list is terminated by a double <b>null</b>.

### -field PortalGroups

A <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portal_groupa">ISCSI_TARGET_PORTAL_GROUP</a> structure that contains descriptions of the portals in the portal group associated with the target.

### -field PersistentTargetMappings

An array of <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a> structures that contains information about the HBAs and buses through which the target can be reached. The array is preceded by a <b>ULONG</b> value that contains the number of elements in the array. Each <b>ISCSI_TARGET_MAPPING</b> structure is aligned on a 4-byte boundary.

### -field InitiatorName

A <b>null</b>-terminated string that contains the initiator HBA that connects to the target.

### -field TargetFlags

The flags associated with the target. The following table lists the flags that can be associated with a target.

<table>
<tr>
<th>Target Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>ISCSI_TARGET_FLAG_HIDE_STATIC_TARGET</td>
<td>The target will not be reported as discovered unless it is also discovered dynamically.</td>
</tr>
</table>

### -field LoginOptions

A value of the <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a> structure that defines the login data.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-getiscsitargetinformationa">GetIScsiTargetInformation</a>

