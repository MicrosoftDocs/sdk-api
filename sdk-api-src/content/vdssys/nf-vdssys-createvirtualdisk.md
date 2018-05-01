---
UID: NF:vdssys.CreateVirtualDisk
title: CreateVirtualDisk function
author: windows-driver-content
description: Creates a virtual disk using the resources of the storage pool.
old-location: stormgmt\createvirtualdisk_msft_storagepool.htm
old-project: stormgmt
ms.assetid: 1a5bf78d-356c-44a7-8f76-2cad85d3c171
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: Composite VirtualDisk Member, Composite Volume Member, CreateVirtualDisk, CreateVirtualDisk method [Windows Storage Management API], CreateVirtualDisk method [Windows Storage Management API], MSFT_StoragePool class, Delta Replica Target, Element Component, Fixed, Local Replica Source, Local Replica Source or Target, Local Replica Target, MSFT_StoragePool class [Windows Storage Management API], CreateVirtualDisk method, MSFT_StoragePool.CreateVirtualDisk, Other, Remote Replica Source, Remote Replica Source or Target, Remote Replica Target, Reserved as Pool Contributor, Reserved by Migration Services, Reserved by Replication Services, Reserved for ComputerSystem (the block server), Reserved for Sparing, Thin, Unknown, Unrestricted, stormgmt.createvirtualdisk_msft_storagepool
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vdssys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Root\Microsoft\Windows\Storage
req.assembly: 
req.type-library: 
req.typenames: RAW_SCSI_VIRTUAL_DISK_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	vdssys.h
api_name:
-	MSFT_StoragePool.CreateVirtualDisk
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# CreateVirtualDisk function


## -description


Creates a virtual disk using the resources of the storage pool.


## -parameters




### -param VirtualStorageType

TBD


### -param Path

TBD


### -param VirtualDiskAccessMask

TBD


### -param SecurityDescriptor

TBD


### -param Flags

TBD


### -param ProviderSpecificFlags

TBD


### -param Parameters

TBD


### -param Overlapped

TBD


### -param Handle

TBD




#### - AutoNumberOfColumns [in]

If <b>TRUE</b>, this field instructs the storage provider (or subsystem) to automatically choose what it determines to be the best number of columns for the virtual disk. If this field is <b>TRUE</b>,  the <i>NumberOfColumns</i> parameter must be <b>NULL</b>.


#### - AutoWriteCacheSize [in]

<b>TRUE</b> if the provider should pick up the auto write cache size; otherwise, <b>FALSE</b>.


#### - CreatedStorageJob [out]

If <i>RunAsJob</i> is set to <b>TRUE</b> and this method takes a long time to execute, this parameter receives a reference to the storage job object that is used to track the long-running operation.


#### - CreatedVirtualDisk [out]

Receives a <a href="https://msdn.microsoft.com/4f0d6967-ab9c-494f-a991-f62fda8c2fa8">MSFT_VirtualDisk</a> object if this method is run normally (with <i>RunAsJob</i> set to <b>FALSE</b>) and the virtual disk is successfully created.


#### - ExtendedStatus [out]

A string that contains an embedded <a href="https://msdn.microsoft.com/BD1268B5-A1B6-4ADB-90FA-C270E23B4844">MSFT_StorageExtendedStatus</a> object.

This parameter allows the storage provider to return extended (implementation-specific) error information.


#### - FriendlyName [in]

The friendly name for the virtual disk.

Friendly names are expected to be descriptive, but they are not required to be unique. Note that some storage pools do not allow setting a friendly name during virtual disk creation. If a storage pool doesn't support this, virtual disk creation should still succeed, however the virtual disk may have a different name assigned to it.

This parameter is required and cannot be <b>NULL</b>.


#### - Interleave [in]

Specifies the number of bytes that should for a strip in the common striping-based resiliency settings. The strip is defined as the size of the portion of a stripe that lies on one physical disk. Thus <i>Interleave</i> * <i>NumberOfColumns</i> will yield the size of one stripe of user data.

If this parameter is specified, this value will override the <b>InterleaveDefault</b> which would have been inherited from the resiliency setting specified by <i>ResiliencySettingName</i>.


#### - IsEnclosureAware [in]

Determines the allocation behavior for this virtual disk. Enclosure aware virtual disks will intelligently pick the physical disks to use for their redundancy. If <b>TRUE</b>, the virtual disk will attempt to use physical disks from different enclosures to balance the fault tolerance between two or more physical enclosures.


#### - NumberOfColumns [in]

Specifies the number of underlying physical disks across which data should be striped. If specified, this value will override the <b>NumberOfColumnsDefault</b> which would have been inherited from the resiliency setting specified by <i>ResiliencySettingName</i>.


#### - NumberOfDataCopies [in]

Specifies the number of complete data copies to maintain for the virtual disk.

If specified, this value will override the <b>NumberOfDataCopiesDefault</b> which would have been inherited from the resiliency setting specified by <i>ResiliencySettingName</i>.


#### - OtherUsageDescription [in]

A vendor specific usage for the new virtual disk. This parameter can only be specified if the <b>Usage</b> property is set to <b>Other</b>.


#### - PhysicalDiskRedundancy [in]

Specifies how many physical disk failures the virtual disk should be able to withstand before data loss occurs. If specified, this value will override the <b>PhysicalDiskRedundancyDefault</b> which would have been inherited from the resiliency setting specified by <i>ResiliencySettingName</i>.


#### - PhysicalDisksToUse [in]

If this parameter contains a list of physical disks, allocation of this virtual disk's storage is limited to the physical disks in the list. These physical disks must already be added to this storage pool.


#### - ProvisioningType [in]

Specifies the provisioning type for the virtual disk.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Unknown"></a><a id="unknown"></a><a id="UNKNOWN"></a><dl>
<dt><b>Unknown</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The provisioning type is unknown. This could mean that this information is unavailable, or that the storage subsystem uses a proprietary method of allocation.

</td>
</tr>
<tr>
<td width="40%"><a id="Thin"></a><a id="thin"></a><a id="THIN"></a><dl>
<dt><b>Thin</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The storage for the virtual disk is allocated on demand.

</td>
</tr>
<tr>
<td width="40%"><a id="Fixed"></a><a id="fixed"></a><a id="FIXED"></a><dl>
<dt><b>Fixed</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The storage for the virtual disk is allocated when the disk is created.

</td>
</tr>
</table>
 


#### - ResiliencySettingName [in]

The desired resiliency setting to use as a template for this virtual disk. This parameter's value should correspond to the particular <a href="https://msdn.microsoft.com/8F8981DB-50D7-424D-BD5B-C646FD8E434F">MSFT_ResiliencySetting</a> object's <b>Name</b> property. Only resiliency settings associated with this storage pool may be used.


#### - RunAsJob [in]

If <b>TRUE</b>, this method uses the <i>CreatedStorageJob</i> parameter when the request is taking a long time to service. If a storage job has been created to track the operation, this method will return <b>Method Parameters Checked - Job Started</b>. <div class="alert"><b>Note</b>  Even if <i>RunAsJob</i> is <b>TRUE</b>, this method can still return a result if it has finished in sufficient time.</div>
<div> </div>


If <b>FALSE</b> or <b>NULL</b>, this method will follow default WMI asynchronous behavior as determined by the client's method for invocation. In other words, it is synchronous unless requested otherwise.


#### - Size [in]

Indicates the desired size, in bytes, of the virtual disk. Note that some storage subsystems will round the size up or down to a multiple of its allocation unit size. On output, this parameter indicates the actual size of the virtual disk that was created. This parameter cannot be used if <i>UseMaximumSize</i> is set to <b>TRUE</b>.


#### - StorageTierSizes [in]

Sizes of the storage tiers.


#### - StorageTiers [in]

Storage tiers on this virtual disk. Each element of the array is an <a href="https://msdn.microsoft.com/0E049D07-DD37-4F64-8483-3ECF32211567">MSFT_StorageTier</a> object.


#### - Usage [in]

Specifies the intended usage for the virtual disk.

You can specify a  predefined description or a custom description. To specify a predefined description, use a value other than <b>Other</b>. 

To specify a custom description, use <b>Other</b> and specify a non-NULL value for the <b>OtherUsageDescription</b> property.



#### Other (1)



#### Unrestricted (2)



#### Reserved for ComputerSystem (the block server) (3)



#### Reserved by Replication Services (4)



#### Reserved by Migration Services (5)



#### Local Replica Source (6)



#### Remote Replica Source (7)



#### Local Replica Target (8)



#### Remote Replica Target (9)



#### Local Replica Source or Target (10)



#### Remote Replica Source or Target (11)



#### Delta Replica Target (12)



#### Element Component (13)



#### Reserved as Pool Contributor (14)



#### Composite Volume Member (15)



#### Composite VirtualDisk Member (16)



#### Reserved for Sparing (17)


#### - UseMaximumSize [in]

If <b>TRUE</b>, this parameter instructs the storage array to create the largest possible virtual disk given the available resources of this storage pool. This parameter cannot be used if the <i>Size</i> parameter is set.


#### - WriteCacheSize [in]

Size of write cache on the virtual disk.


## -returns



This function returns DWORD.




## -remarks



This method is only available when the <b>SupportsVirtualDiskCreation</b> property on the storage subsystem is set to <b>TRUE</b>. If it is set to <b>FALSE</b>, this method will fail with <b>MI_RESULT_NOT_SUPPORTED</b>. 

This method is not supported for primordial pools.

This method only requires a <i>FriendlyName</i> and <i>Size</i> to be specified. Sizes can be specified explicitly through the <i>Size</i> parameter, or told to use the maximum available space from the storage pool by using the <i>UseMaximumSize</i> parameter. Both <i>FriendlyName</i> and <i>Size</i> are treated as goals rather than hard requirements. For example, not all SMI-S based arrays may support custom friendly names, however the virtual disk creation will still succeed. If the size specified is not achieved, then the actual size used for the virtual disk will be returned in the out parameter structure.

The usage of this virtual disk can be set using the <i>Usage</i> and <i>OtherUsageDescription</i> parameters. If a value for <i>OtherUsageDescription</i> is given, <i>Usage</i> must be set to 1 - 'Other', otherwise an error will be returned.

By default, the resiliency setting applied to this virtual disk will be whatever is specified in the storage pool's <b>ResiliencySettingNameDefault</b> property. This can be overridden using the <i>ResiliencySettingName</i> parameter. Note that the name given here must correspond to a resiliency setting associated with this storage pool. Any other value will result in an error.

Individual settings of the resiliency setting can be overridden using the <i>NumberOfDataCopies</i>, <i>PhysicalDiskRedundancy</i>, <i>NumberOfColumns</i>, and <i>Interleave</i> parameters. If these parameters are not used, the defaults from the resiliency setting will be used. These overrides will not persist back to the particular resiliency setting instance; however some storage providers may choose to create a new resiliency setting instance to capture this new configuration. If any of the goals specified in the override parameters are out of range, or are not supported by the storage pool, an error will be returned.

The provisioning policy for the virtual disk is determined in a similar way to the resiliency setting. If no preference is specified in the <i>ProvisioningType</i> parameter, the policy is determined by the storage pool's <b>ProvisioningTypeDefault</b> property. If the <i>ProvisioningType</i> parameter is specified, the default is ignored and the value specified will be used instead.

Allocation can be further controlled by the <i>PhysicalDisksToUse</i> parameter. There may be certain scenarios where a storage administrator wants to manually choose which physical disks should back the virtual disk. When this parameter is specified, data for the virtual disk will only be stored on the physical disks in this array and not on any others.




## -see-also




<a href="https://msdn.microsoft.com/135414e0-3e43-4ee4-ab5d-1ec5aceb5695">MSFT_StoragePool</a>
 

 

