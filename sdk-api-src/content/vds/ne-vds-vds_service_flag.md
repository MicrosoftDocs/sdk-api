---
UID: NE:vds._VDS_SERVICE_FLAG
title: VDS_SERVICE_FLAG (vds.h)
author: windows-sdk-content
description: Defines the set of valid flags for the service object.
old-location: base\vds_service_flag.htm
tech.root: VDS
ms.assetid: d14718bd-43a3-4775-a218-27c59f6995eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_SERVICE_FLAG, VDS_SERVICE_FLAG enumeration [VDS], VDS_SVF_AUTO_MOUNT_OFF, VDS_SVF_CLUSTER_SERVICE_CONFIGURED, VDS_SVF_EFI, VDS_SVF_OS_UNINSTALL_VALID, VDS_SVF_SUPPORT_DYNAMIC, VDS_SVF_SUPPORT_DYNAMIC_1394, VDS_SVF_SUPPORT_FAULT_TOLERANT, VDS_SVF_SUPPORT_GPT, VDS_SVF_SUPPORT_MIRROR, VDS_SVF_SUPPORT_RAID5, base.vds_service_flag, vds/VDS_SERVICE_FLAG, vds/VDS_SVF_AUTO_MOUNT_OFF, vds/VDS_SVF_CLUSTER_SERVICE_CONFIGURED, vds/VDS_SVF_EFI, vds/VDS_SVF_OS_UNINSTALL_VALID, vds/VDS_SVF_SUPPORT_DYNAMIC, vds/VDS_SVF_SUPPORT_DYNAMIC_1394, vds/VDS_SVF_SUPPORT_FAULT_TOLERANT, vds/VDS_SVF_SUPPORT_GPT, vds/VDS_SVF_SUPPORT_MIRROR, vds/VDS_SVF_SUPPORT_RAID5
ms.topic: enum
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
api_name:
 - VDS_SERVICE_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_SERVICE_FLAG
req.redist: 
ms.custom: 19H1
---

# VDS_SERVICE_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set 
   of valid flags for the service object.


## -enum-fields




### -field VDS_SVF_SUPPORT_DYNAMIC

If set, the service supports dynamic disks.


### -field VDS_SVF_SUPPORT_FAULT_TOLERANT

If set, the service supports fault-tolerant volumes.


### -field VDS_SVF_SUPPORT_GPT

If set, the service supports GPT disks.


### -field VDS_SVF_SUPPORT_DYNAMIC_1394

If set, the service supports dynamic 1394 disks.


### -field VDS_SVF_CLUSTER_SERVICE_CONFIGURED

If set, the host has the cluster service installed and configured, but not necessarily running.


### -field VDS_SVF_AUTO_MOUNT_OFF

If set, the auto-mount operation is turned off for the computer to prevent the operating system from 
      automatically mounting new partitions.

<div class="alert"><b>Note</b>  Beginning with Windows 8 and Windows Server 2012, this flag is deprecated. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/vds/ne-vds-_vds_san_policy">VDS_SAN_POLICY</a> enumeration to control default disk mounting behavior.</div>
<div> </div>

### -field VDS_SVF_OS_UNINSTALL_VALID

If set, configuration changes to VDS have occurred. After a successful installation, the uninstall 
      operation is valid only if the configuration changes.


### -field VDS_SVF_EFI

If set, the machine boots from an EFI partition on a GPT disk.

<b>Windows Server 2003:  </b>This flag is not supported before Windows Server 2003 with SP1.


### -field VDS_SVF_SUPPORT_MIRROR

The service supports mirrored volumes.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDS_SVF_SUPPORT_RAID5

The service supports RAID-5 volumes.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDS_SVF_SUPPORT_REFS




## -remarks



This enumeration provides the values for the <i>ulFlags</i> member of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_service_prop">VDS_SERVICE_PROP</a> structure. The 
    <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-setflags">IVdsService::SetFlags</a> method passes the value as an 
    argument to set the <b>VDS_SVF_AUTO_MOUNT_OFF</b> flag.

<b>Windows Server 2003:  </b>Many of these enumerators are specific to the Windows Server 2003 platform, which supports 
      both 1394 and USB devices.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_SERVICE_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_SERVICE_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_service_prop">VDS_SERVICE_PROP</a>
 

 

