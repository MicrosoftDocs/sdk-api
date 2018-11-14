---
UID: NS:vds._VDS_LUN_PROP
title: "_VDS_LUN_PROP"
author: windows-sdk-content
description: Defines the properties of a LUN object.
old-location: base\vds_lun_prop.htm
tech.root: VDS
ms.assetid: 4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PVDS_LUN_PROP, PVDS_LUN_PROP, PVDS_LUN_PROP structure pointer [VDS], VDS_H_FAILED, VDS_H_FAILED_REDUNDANCY, VDS_H_FAILED_REDUNDANCY_FAILING, VDS_H_FAILING, VDS_H_FAILING_REDUNDANCY, VDS_H_HEALTHY, VDS_H_REBUILDING, VDS_H_UNKNOWN, VDS_LUN_PROP, VDS_LUN_PROP structure [VDS], _VDS_LUN_PROP, base.vds_lun_prop, vds/PVDS_LUN_PROP, vds/_VDS_LUN_PROP, vdshwprv/PVDS_LUN_PROP, vdshwprv/_VDS_LUN_PROP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_LUN_PROP
product: Windows
targetos: Windows
req.typenames: VDS_LUN_PROP, *PVDS_LUN_PROP
req.redist: 
---

# _VDS_LUN_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of 
   a <a href="https://msdn.microsoft.com/ea22bd6d-4a7a-4674-82e9-08460914ff8e">LUN object</a>.


## -struct-fields




### -field id

The GUID of the LUN object.


### -field ullSize

The size of the LUN, in bytes.


### -field pwszFriendlyName

The name of the LUN; a zero-terminated, human-readable string.


### -field pwszIdentification

The unique LUN identifier; a zero-terminated, human-readable string.


### -field pwszUnmaskingList

A list specifying the computers on the network to be granted access the LUN; a semicolon-delimited, 
      NULL-terminated, human-readable string. 

If the value is "*", all computers on the network are to be granted 
      access to the LUN. If the value is "", no computers are to be granted access to the LUN.

<div class="alert"><b>Note</b>  In practice, if the value is "*", most hardware providers only grant the ports and initiators on the local computer access to the LUN.</div>
<div> </div>
If "*" or "" is specified, no other value can be specified.

For Fibre Channel networks and serial attached SCSI (SAS) networks, each entry is a 64-bit World-Wide Name (WWN) of each port to which the LUN is unmasked, 
       formatted as a hexadecimal string (16 characters long), most significant byte first. For 
       example, a WWN address of 01:23:45:67:89:AB:CD:EF is represented as "0123456789ABCDEF". For more information, see the T10 specifications for <a href="http://go.microsoft.com/fwlink/p/?linkid=179932">Fibre Channel</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=179931">SAS</a>.

For iSCSI networks, each entry is an iSCSI qualified name (IQN) of each initiator to which the LUN is unmasked. A LUN unmasked 
       to a particular initiator is considered to be associated with that initiator.

<div class="alert"><b>Note</b>  The unmasking list can contain the same WWN or IQN more than once. Duplicates are ignored.</div>
<div> </div>

### -field ulFlags

The LUN flags enumerated by <a href="https://msdn.microsoft.com/977ee10c-c91f-4510-bf00-6b7d4da6c1c0">VDS_LUN_FLAG</a>.


### -field type

The LUN type enumerated by <a href="https://msdn.microsoft.com/0952db7d-9dd6-4602-82d4-66d773c14463">VDS_LUN_TYPE</a>.


### -field status

The status of the LUN object enumerated by 
      <a href="https://msdn.microsoft.com/dac82973-d8c0-430b-aeea-163af7d94d24">VDS_LUN_STATUS</a>.


### -field health

A 
      <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> enumeration value that specifies the health state of the LUN. The following are the valid values for this member.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_REBUILDING (2)



#### VDS_H_FAILING (4)



#### VDS_H_FAILING_REDUNDANCY (5)



#### VDS_H_FAILED_REDUNDANCY (6)



#### VDS_H_FAILED_REDUNDANCY_FAILING (7)



#### VDS_H_FAILED (8)


### -field TransitionState

The transition state of the LUN enumerated by
      <a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a>.


### -field sRebuildPriority

The rebuild priority of the LUN object. A value between 0 (lowest priority) and 15 (highest priority).


## -remarks



The <a href="https://msdn.microsoft.com/1fec1c8d-7ac9-4b77-830c-930908aac6ef">IVdsLun::GetProperties</a> method returns 
    this structure to report the properties of a <a href="https://msdn.microsoft.com/ea22bd6d-4a7a-4674-82e9-08460914ff8e">LUN object</a>.




## -see-also




<a href="https://msdn.microsoft.com/1fec1c8d-7ac9-4b77-830c-930908aac6ef">IVdsLun::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>



<a href="https://msdn.microsoft.com/dac82973-d8c0-430b-aeea-163af7d94d24">VDS_LUN_STATUS</a>



<a href="https://msdn.microsoft.com/0952db7d-9dd6-4602-82d4-66d773c14463">VDS_LUN_TYPE</a>



<a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a>
 

 

