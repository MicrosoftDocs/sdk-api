---
UID: NE:iscsidsc.__unnamed_enum_4
title: TARGET_INFORMATION_CLASS (iscsidsc.h)
author: windows-sdk-content
description: TARGET_INFORMATION_CLASS enumeration specifies information about the indicated target device that the GetIScsiTargetInformation function retrieves.
old-location: iscsidisc\target_information_class.htm
tech.root: iSCSIDisc
ms.assetid: 2ef6cff7-b5ab-463d-b274-62be81bc9295
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTARGET_INFORMATION_CLASS, DiscoveryMechanism, InitiatorName, LoginOptions, PersistentTargetMappings, PortalGroups, ProtocolType, TARGET_INFORMATION_CLASS, TARGET_INFORMATION_CLASS enumeration [iSCSI Discovery Library API], TargetAlias, TargetFlags, iscsidisc.target_information_class, iscsidsc/DiscoveryMechanism, iscsidsc/InitiatorName, iscsidsc/LoginOptions, iscsidsc/PersistentTargetMappings, iscsidsc/PortalGroups, iscsidsc/ProtocolType, iscsidsc/TARGET_INFORMATION_CLASS, iscsidsc/TargetAlias, iscsidsc/TargetFlags"
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - TARGET_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
req.redist: 
---

# TARGET_INFORMATION_CLASS enumeration


## -description


The <b>TARGET_INFORMATION_CLASS</b> enumeration specifies information about the indicated target device that the <a href="https://msdn.microsoft.com/3db31d0b-ed08-432b-9c28-a700c4a9d369">GetIScsiTargetInformation</a> function retrieves.



## -enum-fields




### -field ProtocolType

A value of the <a href="https://msdn.microsoft.com/1997b1d0-6723-434c-bca7-513e4dc30ee6">TARGETPROTOCOLTYPE</a> structure, indicating the protocol that the initiator uses to communicate with the target device. 



### -field TargetAlias

A <b>null</b>-terminated string that contains the alias of the target device. 



### -field DiscoveryMechanisms


### -field PortalGroups

A <a href="https://msdn.microsoft.com/8b7e874b-5d2b-4948-98f2-1bcd6d4f8ca6">ISCSI_TARGET_PORTAL_GROUP</a> structure that contains descriptions of the portals in the portal group associated with the target. 



### -field PersistentTargetMappings

An array of <a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a> structures that contains information about the HBAs and buses through which the target can be reached. The array is preceded by a <b>ULONG</b> value that contains the number of elements in the array. Each <b>ISCSI_TARGET_MAPPING</b> structure is aligned on a 4-byte boundary. 



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

A value of the <a href="https://msdn.microsoft.com/7d45be86-3d85-4253-aef7-92e05379f1b2">ISCSI_LOGIN_OPTIONS</a> structure that defines the login data.


#### - DiscoveryMechanism

A list of <b>null</b>-terminated strings that describe the discovery mechanisms that located the indicated target. The list is terminated by a double <b>null</b>. 



## -see-also




<a href="https://msdn.microsoft.com/3db31d0b-ed08-432b-9c28-a700c4a9d369">GetIScsiTargetInformation</a>
 

 

