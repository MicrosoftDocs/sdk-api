---
UID: NF:vsprov.IVssHardwareSnapshotProvider.FillInLunInfo
title: IVssHardwareSnapshotProvider::FillInLunInfo
author: windows-sdk-content
description: Prompts the hardware provider to indicate whether it supports the corresponding disk device and correct any omissions in the VDS_LUN_INFORMATION structure.
old-location: base\ivsshardwaresnapshotprovider_fillinluninfo.htm
old-project: VSS
ms.assetid: 4e4e5942-5bc8-4b5e-a651-5bb354514994
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FillInLunInfo, FillInLunInfo method [VSS], FillInLunInfo method [VSS],IVssHardwareSnapshotProvider interface, IVssHardwareSnapshotProvider interface [VSS],FillInLunInfo method, IVssHardwareSnapshotProvider.FillInLunInfo, IVssHardwareSnapshotProvider::FillInLunInfo, base.ivsshardwaresnapshotprovider_fillinluninfo, vsprov/IVssHardwareSnapshotProvider::FillInLunInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: VSS_VOLUME_PROTECTION_INFO, *PVSS_VOLUME_PROTECTION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssHardwareSnapshotProvider.FillInLunInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssHardwareSnapshotProvider::FillInLunInfo


## -description


The 
   <b>FillInLunInfo</b> 
   method prompts the hardware provider to indicate whether it supports the corresponding disk device and correct any omissions in the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure. VSS calls the 
   <b>FillInLunInfo</b> 
   method after the 
   <a href="https://msdn.microsoft.com/9a996875-a495-43c1-987e-67c31d0651c7">IVssHardwareSnapshotProvider::LocateLuns</a> method or before 
   the <a href="https://msdn.microsoft.com/06a31704-9031-4ab9-84eb-685f6b648d27">IVssHardwareSnapshotProvider::OnLunEmpty</a> method to obtain the 
   <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure associated with a 
   shadow copy LUN. VSS will compare the 
   <b>VDS_LUN_INFORMATION</b> structure received in 
   the <a href="https://msdn.microsoft.com/299020eb-0afd-41c8-9551-1275eff45fa1">IVssHardwareSnapshotProvider::GetTargetLuns</a> method to identify 
   shadow copy LUNs. If the structures do not match, the requester will receive 
   <b>VSS_S_SOME_SNAPSHOTS_NOT_IMPORTED</b>, which indicates a mismatch.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters




### -param wszDeviceName [in]

Device corresponding to the shadow copy LUN.


### -param pLunInfo [in, out]

The <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure for the 
      shadow copy LUN.


### -param pbIsSupported [out]

The provider must return <b>TRUE</b> in the location pointed to by the 
      <i>pbIsSupported</i> parameter if the device is supported.


## -returns



VSS  ignores this method's return value.

<b>Windows Server 2003:  </b>VSS does not ignore the return value, which can be one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000EL</dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An unexpected provider error has occurred. The provider must report an event in the application event log 
        providing the user with information on how to resolve the problem.

</td>
</tr>
</table>
 




## -remarks



VSS calls the <b>FillInLunInfo</b> method for each <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure that the provider previously initialized in its <a href="https://msdn.microsoft.com/299020eb-0afd-41c8-9551-1275eff45fa1">GetTargetLuns</a> method. VSS also calls the <b>FillInLunInfo</b> method for each new disk device that arrives in the system during the import process. 

The provider can correct any omissions in the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure received in the <i>pLunInfo</i>  parameter. However, the provider should not modify the value of the <b>m_rgInterconnects</b> member of this structure.

The members of the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure correspond to the SCSI Inquiry Data and Vital Product Data page 80 (device serial number) information, with the following exceptions:

<ul>
<li>The <b>m_version</b> member must be set to <b>VER_VDS_LUN_INFORMATION</b>.</li>
<li>The <b>m_BusType</b> member is ignored in comparisons during import. This value depends on the PnP storage stack on the corresponding disk device. Usually this is <b>VDSBusTypeScsi</b>.</li>
<li>The <b>m_diskSignature</b> member is ignored in comparisons during import. The provider must set this member to GUID_NULL.</li>
</ul>
The members of the <a href="https://msdn.microsoft.com/88fe83cb-6d3c-40bd-a5ce-71771d2e7511">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a> 
      structure (in the <b>m_deviceIdDescriptor</b> member of the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> 
    structure) correspond to the page 83 information. In this structure, each <a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a> 
      structure corresponds to the STORAGE_IDENTIFIER structure for a device identifier (that is, a storage identifier with an association type of zero). For more information about the STORAGE_IDENTIFIER structure, see the Windows Driver Kit (WDK) documentation.

If the <b>FillInLunInfo</b> method is 
    called for a LUN that is unknown to the provider, the provider should not return an error. Instead, it 
    should return <b>FALSE</b>  in the <b>BOOL</b> value that the <i>pbIsSupported</i> parameter points to and 
    return success. If the provider recognizes the LUN, it should set the <b>BOOL</b> value to 
    <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/f3615770-63a1-49eb-a3b9-b4d349fc33df">AreLunsSupported</a>



<a href="https://msdn.microsoft.com/299020eb-0afd-41c8-9551-1275eff45fa1">GetTargetLuns</a>



<a href="https://msdn.microsoft.com/97fbb6bf-110e-4393-bf25-1ec378b91bdc">IVssHardwareSnapshotProvider</a>



<a href="https://msdn.microsoft.com/9a996875-a495-43c1-987e-67c31d0651c7">LocateLuns</a>



<a href="https://msdn.microsoft.com/06a31704-9031-4ab9-84eb-685f6b648d27">OnLunEmpty</a>



<a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>



<a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a>
 

 

