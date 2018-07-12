---
UID: NE:vds._VDS_SAN_POLICY
title: "_VDS_SAN_POLICY"
author: windows-sdk-content
description: Defines the set of valid disk SAN policy flags.
old-location: base\vds_san_policy.htm
old-project: vds
ms.assetid: 2da99388-8ee6-4e6b-98dc-52f12290c4dc
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: VDS_SAN_POLICY, VDS_SAN_POLICY enumeration, VDS_SP_OFFLINE, VDS_SP_OFFLINE_SHARED, VDS_SP_ONLINE, VDS_SP_UNKNOWN, _VDS_SAN_POLICY, base.vds_san_policy, vds/VDS_SAN_POLICY, vds/VDS_SP_OFFLINE, vds/VDS_SP_OFFLINE_SHARED, vds/VDS_SP_ONLINE, vds/VDS_SP_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
tech.root: 
req.typenames: VDS_SAN_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_SAN_POLICY
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_SAN_POLICY enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid disk SAN policy flags.


## -enum-fields




### -field VDS_SP_UNKNOWN

The SAN policy is unknown.


### -field VDS_SP_ONLINE

All newly discovered disks are brought online and made read-write.


### -field VDS_SP_OFFLINE_SHARED

All newly discovered disks that do not reside on a shared bus are brought online and made read-write.


### -field VDS_SP_OFFLINE

All newly discovered disks remain offline and read-only.


### -field VDS_SP_OFFLINE_INTERNAL


### -field VDS_SP_MAX




## -remarks



The SAN policy determines whether a newly discovered disk is brought online or remains offline, and whether it is made read/write or remains read-only. When a disk is offline, the disk layout can be read, but no volume devices are surfaced through Plug and Play (PnP). This means that no file system can be mounted on the disk. When a disk is online, one or more volume devices are installed for the disk.

To query the current SAN policy, use the <a href="https://msdn.microsoft.com/59602d97-2fdf-4d1b-b158-e545619397e0">IVdsServiceSAN::GetSANPolicy</a> method.

To set the SAN policy, use the <a href="https://msdn.microsoft.com/e5cb0b5e-d181-44a7-8416-e9f8fb575423">IVdsServiceSAN::SetSANPolicy</a> method.

This enumeration supersedes the <b>NoAutoMount</b> registry key, which can be found under the following registry path:

<b>HKEY_LOCAL_MACHINE</b>\<b>System</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>Mountmgr</b>\<b>NoAutoMount</b>

The value of this key is a REG_DWORD value that is set to 0x00000000 to enable the Windows automount feature or a nonzero value to disable it. If the automount feature is enabled, Windows automatically mounts the file system for a new basic volume when it is added to the system and then assigns a drive letter to the volume. In system area network configurations, disabling automount prevents Windows from automatically mounting or assigning drive letters to any new basic volumes that are added to the system.

On Windows Server 2016, the default SAN policy is <b>VDS_SP_OFFLINE_SHARED</b>. This applies to all editions and installation types, including Nano Server.

On Windows Server 2008 Enterprise and Windows Server 2008 Datacenter, the default SAN policy is <b>VDS_SP_OFFLINE_SHARED</b>. On all other Windows Server 2008 editions, the default SAN policy is <b>VDS_SP_ONLINE</b>.

For an upgrade from an earlier version of Windows, if the <b>NoAutoMount</b> registry key was set before the upgrade, the upgrade will clear this registry key and set the SAN policy to <b>VDS_SP_OFFLINE_SHARED</b>. (The <b>NoAutoMount</b> registry key is set by default on Windows Server 2008 Enterprise and Windows Server 2008 Datacenter.) If the <b>NoAutoMount</b> registry key was not set before the upgrade, the upgrade will set the SAN policy to <b>VDS_SP_ONLINE</b>. In addition, the upgrade checks each disk to determine whether the volumes on the disk are online or offline. If a disk is online before the upgrade and has one or more online volumes, the upgrade will bring that disk and all of its volumes online, regardless of the SAN policy or whether the disk resides on a shared bus. For example, suppose that an online disk with two offline volumes and one online volume resides on a shared bus, and the <b>NoAutoMount</b> registry key is set before the upgrade. After the upgrade, the SAN policy will be <b>VDS_SP_OFFLINE_SHARED</b>, the disk will be brought online, and all three volumes will be brought online.

For a clean installation of Windows, the SAN policy determines whether a disk is online or offline after Windows is installed.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_SAN_POLICY</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_SAN_POLICY</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/59602d97-2fdf-4d1b-b158-e545619397e0">IVdsServiceSAN::GetSANPolicy</a>



<a href="https://msdn.microsoft.com/e5cb0b5e-d181-44a7-8416-e9f8fb575423">IVdsServiceSAN::SetSANPolicy</a>
 

 

