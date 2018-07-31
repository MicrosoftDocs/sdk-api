---
UID: NS:vdshwprv._VDS_ASYNC_OUTPUT
title: "_VDS_ASYNC_OUTPUT"
author: windows-sdk-content
description: Defines the output of an async object. Output elements vary depending on the operation type.
old-location: base\vds_async_output.htm
old-project: VDS
ms.assetid: 21771c6a-eca9-47f3-b6fc-383bca1e11bf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: VDS_ASYNCOUT_BREAKVOLUMEPLEX, VDS_ASYNCOUT_CREATELUN, VDS_ASYNCOUT_CREATEPARTITION, VDS_ASYNCOUT_CREATEPORTALGROUP, VDS_ASYNCOUT_CREATETARGET, VDS_ASYNCOUT_CREATEVOLUME, VDS_ASYNCOUT_CREATE_VDISK, VDS_ASYNC_OUTPUT, VDS_ASYNC_OUTPUT structure [VDS], _VDS_ASYNC_OUTPUT, base.vds_async_output, vds/_VDS_ASYNC_OUTPUT, vdshwprv/_VDS_ASYNC_OUTPUT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vdshwprv.h
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
tech.root: 
req.typenames: VDS_ASYNC_OUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_ASYNC_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_ASYNC_OUTPUT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   output of an async object. Output elements vary depending on the operation type.


## -struct-fields




### -field type

Discriminant for the union enumerated by 
      <a href="https://msdn.microsoft.com/c2c0403a-30b9-4619-8bcb-3b73b637509e">VDS_ASYNC_OUTPUT_TYPE</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATEPARTITION"></a><a id="vds_asyncout_createpartition"></a><dl>
<dt><b><b>VDS_ASYNCOUT_CREATEPARTITION</b></b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cp</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATEVOLUME"></a><a id="vds_asyncout_createvolume"></a><dl>
<dt><b><b>VDS_ASYNCOUT_CREATEVOLUME</b></b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cv</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_BREAKVOLUMEPLEX"></a><a id="vds_asyncout_breakvolumeplex"></a><dl>
<dt><b><b>VDS_ASYNCOUT_BREAKVOLUMEPLEX</b></b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>bvp</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATELUN"></a><a id="vds_asyncout_createlun"></a><dl>
<dt><b><b>VDS_ASYNCOUT_CREATELUN</b></b></dt>
<dt>50</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cl</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATETARGET"></a><a id="vds_asyncout_createtarget"></a><dl>
<dt><b><b>VDS_ASYNCOUT_CREATETARGET</b></b></dt>
<dt>62</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>ct</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATEPORTALGROUP"></a><a id="vds_asyncout_createportalgroup"></a><dl>
<dt><b><b>VDS_ASYNCOUT_CREATEPORTALGROUP</b></b></dt>
<dt>63</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cpg</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATE_VDISK"></a><a id="vds_asyncout_create_vdisk"></a><dl>
<dt><b><b>VDS_ASYNCOUT_CREATE_VDISK</b></b></dt>
<dt>200</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cvd</b> structure.

</td>
</tr>
</table>
 


### -field cp

Structure used for the 
       <a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a> or
       <a href="https://msdn.microsoft.com/c9ab5a24-b0b3-41cc-a4bf-3619f156008c">IVdsCreatePartitionEx::CreatePartitionEx</a> 
       method.


### -field cp.ullOffset

Actual offset of the created partition. This may not be the same as the 
        <i>ullOffset</i> parameter passed to the 
        <a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a> or 
        <a href="https://msdn.microsoft.com/c9ab5a24-b0b3-41cc-a4bf-3619f156008c">IVdsCreatePartitionEx::CreatePartitionEx</a> 
        method.


### -field cp.volumeId

The ID of the <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">volume object</a> associated with the 
        created partition.


### -field cv

Structure used for the 
       <a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a> method.


### -field cv.pVolumeUnk


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> for the volume object. For more information, see 
        <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">Volume Object</a>.


### -field bvp

Structure used for the <a href="https://msdn.microsoft.com/c7e42aa4-3233-40e9-b537-043eecd192ad">IVdsVolume::BreakPlex</a> 
       method.


### -field bvp.pVolumeUnk


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> for the volume object. For more information, see 
        <a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">Volume Object</a>.
       


### -field sv

Structure used for the <a href="https://msdn.microsoft.com/63ac6ef9-0e84-40ed-a302-4f32316a41cc">IVdsVolume::Shrink</a> 
       method.


### -field sv.ullReclaimedBytes

The number of bytes that were reclaimed by the shrink operation.

<b>Windows Server 2003:  </b> This member is not supported until Windows Server 2003 R2.


### -field cl

Structure used for the 
       <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> method.


### -field cl.pLunUnk


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> for the LUN object. For more information, see 
        <a href="https://msdn.microsoft.com/ea22bd6d-4a7a-4674-82e9-08460914ff8e">LUN Object</a>.


### -field ct

Structure used for the 
       <a href="https://msdn.microsoft.com/084a1f0e-0764-404a-bd9a-a724e4f12c5f">IVdsSubSystemIscsi::CreateTarget</a> method.


### -field ct.pTargetUnk


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> for the target object. 
        For more information, see the <a href="https://msdn.microsoft.com/e88d65ad-9b56-4620-a0f5-573c5e245b3e">Target Object</a>.
       


### -field cpg

Structure used for the 
       <a href="https://msdn.microsoft.com/c479b5ee-2e6a-4a3f-bd80-c3c25adac20f">IVdsIscsiTarget::CreatePortalGroup</a> method.


### -field cpg.pPortalGroupUnk


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> for the portal group object. 
        For more information, see the <a href="https://msdn.microsoft.com/e5892e96-b6ad-447a-9627-b44fc6f1b27a">Portal Group Object</a>.
       


### -field cvd

Structure used for the 
       <a href="https://msdn.microsoft.com/3655946d-f8b5-46a1-97e3-82b0831124b3">IVdsVdProvider::CreateVDisk</a> method.


### -field cvd.pVDiskUnk


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> for the virtual disk object.


## -remarks



The <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> method returns this structure 
    and adds a reference to any contained object produced by each method. 
    Callers must release the reference to the contained object.




## -see-also




<a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c2c0403a-30b9-4619-8bcb-3b73b637509e">VDS_ASYNC_OUTPUT_TYPE</a>
 

 

