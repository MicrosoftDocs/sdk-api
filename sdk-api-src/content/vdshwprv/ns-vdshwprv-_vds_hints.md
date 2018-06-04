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

# _VDS_HINTS structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]


   Defines the automagic hints for a 
   LUN or LUN plex.


## -struct-fields




### -field ullHintMask


The LUN hint mask. Each of the <b>BOOL</b> members of this structure has a corresponding hint flag that can be set in the mask. If the 
      hint flag is set, the corresponding hint is considered. If the hint flag is not set, the hint is ignored. The 
      hint flags are described in the following table.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_FASTCRASHRECOVERYREQUIRED"></a><a id="vds_hint_fastcrashrecoveryrequired"></a><dl>
<dt><b>VDS_HINT_FASTCRASHRECOVERYREQUIRED</b></dt>
<dt>0x0000000000000001L</dt>
</dl>
</td>
<td width="60%">
The provider limits the time that is required for recovery. To support fast recovery, the provider uses a change log that enables the provider to recover the LUN without comparing the entire contents of the LUN.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_MOSTLYREADS"></a><a id="vds_hint_mostlyreads"></a><dl>
<dt><b>VDS_HINT_MOSTLYREADS</b></dt>
<dt>0x0000000000000002L</dt>
</dl>
</td>
<td width="60%">
The provider optimizes the LUN for a read-mostly usage pattern, typically by using mirroring rather than parity striping.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_OPTIMIZEFORSEQUENTIALREADS"></a><a id="vds_hint_optimizeforsequentialreads"></a><dl>
<dt><b>VDS_HINT_OPTIMIZEFORSEQUENTIALREADS</b></dt>
<dt>0x0000000000000004L</dt>
</dl>
</td>
<td width="60%">
The provider optimizes the LUN for a sequential-read usage pattern. If this flag is not set and VDS_HINT_OPTIMIZEFORSEQUENTIALWRITES is also not set, the LUN is optimized for random I/O.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_OPTIMIZEFORSEQUENTIALWRITES"></a><a id="vds_hint_optimizeforsequentialwrites"></a><dl>
<dt><b>VDS_HINT_OPTIMIZEFORSEQUENTIALWRITES</b></dt>
<dt>0x0000000000000008L</dt>
</dl>
</td>
<td width="60%">
The provider optimizes the LUN for a sequential-write usage pattern. If this flag is not set and VDS_HINT_OPTIMIZEFORSEQUENTIALREADS is also not set, the LUN is optimized for random I/O.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_READBACKVERIFYENABLED"></a><a id="vds_hint_readbackverifyenabled"></a><dl>
<dt><b>VDS_HINT_READBACKVERIFYENABLED</b></dt>
<dt>0x0000000000000010L</dt>
</dl>
</td>
<td width="60%">
The provider verifies the writes to the LUN by using readback.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_REMAPENABLED"></a><a id="vds_hint_remapenabled"></a><dl>
<dt><b>VDS_HINT_REMAPENABLED</b></dt>
<dt>0x0000000000000020L</dt>
</dl>
</td>
<td width="60%">
The mapping of LUN extents to drive extents is created and updated automatically by the provider. If this flag is not set, the mapping remains fixed after configuration, except when proactive actions are taken to avoid drive failures.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_WRITETHROUGHCACHINGENABLED"></a><a id="vds_hint_writethroughcachingenabled"></a><dl>
<dt><b>VDS_HINT_WRITETHROUGHCACHINGENABLED</b></dt>
<dt>0x0000000000000040L</dt>
</dl>
</td>
<td width="60%">
The provider enables the write-through caching policy on the LUN.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_HARDWARECHECKSUMENABLED"></a><a id="vds_hint_hardwarechecksumenabled"></a><dl>
<dt><b>VDS_HINT_HARDWARECHECKSUMENABLED</b></dt>
<dt>0x0000000000000080L</dt>
</dl>
</td>
<td width="60%">
The provider enables a hardware checksum on the LUN.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_ISYANKABLE"></a><a id="vds_hint_isyankable"></a><dl>
<dt><b>VDS_HINT_ISYANKABLE</b></dt>
<dt>0x0000000000000100L</dt>
</dl>
</td>
<td width="60%">
The provider configures LUN so that the drives that contribute to it can be physically removed with minimal system disruption. This is normally accomplished by ensuring that the LUN occupies as few drives as possible.

</td>
</tr>
</table>
 


### -field ullExpectedMaximumSize


      The maximum size to which the LUN is expected to grow, in bytes. The value can be equal to, greater than, or 
      less than the value specified in <i>ullSizeInBytes</i> when the 
      <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> method is called.
      Some providers use this value to reserve space for the LUN. Providers that are unable to reserve space 
      typically ignore this parameter.


### -field ulOptimalReadSize

The optimal read size for the LUN, in bytes. Zero indicates no optimal read size.


### -field ulOptimalReadAlignment


      The optimal read alignment with respect to the first logical block of the LUN. Zero indicates no optimal read 
      alignment.


### -field ulOptimalWriteSize

The optimal write size for the LUN, in bytes. Zero indicates no optimal write size.


### -field ulOptimalWriteAlignment


      The optimal write alignment with respect to the first logical block of the LUN. Zero indicates no optimal 
      write alignment.


### -field ulMaximumDriveCount


      The maximum number of drives to contribute to the LUN. Zero indicates no maximum drive count. This value can be 
      used to limit the number of stripe interleaves in a stripe set.


### -field ulStripeSize

The mirror or parity stripe interleave size, in bytes. Zero leaves the stripe size unspecified.


### -field bFastCrashRecoveryRequired


      If this member is TRUE, the recovery time is limited. Set the <b>VDS_HINT_FASTCRASHRECOVERYREQUIRED</b> 
      flag in the <b>ullHintMask</b> member to indicate interest in this member.


### -field bMostlyReads


      To optimize for a mostly-reads usage pattern (for example, through mirroring rather than parity striping), set 
      this member to TRUE. Otherwise, set it to <b>FALSE</b>. Set the <b>VDS_HINT_MOSTLYREADS</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.


### -field bOptimizeForSequentialReads


      To optimize for a sequential-reads usage pattern, set this member to <b>TRUE</b>. Otherwise, set it to <b>FALSE</b>. Setting the 
      <b>bOptimizeForSequentialReads</b> and 
      <b>bOptimizeForSequentialWrites</b> members both to <b>FALSE</b> optimizes for random I/O. Set the 
      <b>VDS_HINT_OPTIMIZEFORSEQUENTIALREADS</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.


### -field bOptimizeForSequentialWrites


      To optimize for a sequential-writes usage pattern, set to this member to <b>TRUE</b>. Otherwise, set it to <b>FALSE</b>. Setting the 
      <b>bOptimizeForSequentialReads</b> and 
      <b>bOptimizeForSequentialWrites</b> members both to <b>FALSE</b> optimizes for random I/O. Set the 
      <b>VDS_HINT_OPTIMIZEFORSEQUENTIALWRITES</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.


### -field bRemapEnabled


      If this member is <b>TRUE</b>, the provider remaps LUN extents to drive extents automatically. If it is <b>FALSE</b>, the mapping of LUN extents 
      to drive extents remains fixed after LUN configuration unless extents are explicitly remapped to avoid 
      corrupted blocks. Set the <b>VDS_HINT_REMAPENABLED</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.


### -field bReadBackVerifyEnabled


      If this member is set to <b>TRUE</b>, the provider verifies the writes to the LUN by readback. If it is set to <b>FALSE</b>, the provider does not verify writes. 
      Set the <b>VDS_HINT_READBACKVERIFYENABLED</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.


### -field bWriteThroughCachingEnabled


      If this member is <b>TRUE</b>, the provider enables write-through caching on the LUN. If it is <b>FALSE</b>, the provider does not enable
      write-through caching. Set the <b>VDS_HINT_WRITETHROUGHCACHINGENABLED</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.


### -field bHardwareChecksumEnabled


      If this member is <b>TRUE</b>, the provider enables a checksum on the LUN. Set the 
      <b>VDS_HINT_HARDWARECHECKSUMENABLED</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.


### -field bIsYankable


      If this member is <b>TRUE</b>, the drives that contribute to the LUN can be physically removed without significant disruption to the 
      system (this is typically true when the LUN is composed of extents from only a few drives). If it is <b>FALSE</b>, the LUN
      cannot be removed without significant disruption to the system. Set the 
      <b>VDS_HINT_ISYANKABLE</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.


### -field sRebuildPriority

The rebuild priority for the LUN. The value can range from 0 (lowest priority) through 15 (highest priority).


## -remarks




    The <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> method passes 
    this structure as a parameter to provide hints for creating a LUN. It is passed as a parameter in the 
    <b>ApplyHints</b> method on both the 
    <a href="https://msdn.microsoft.com/e2fbebc0-593e-437c-a401-80e35a43da94">IVdsLun</a> and 
    <a href="https://msdn.microsoft.com/de795ae2-784c-43d7-a34c-546af31d2747">IVdsLunPlex</a> interfaces to apply a new set of hints to a 
    LUN or LUN plex, respectively. Further, it is returned by the <b>QueryHints</b> method on both 
    the <b>IVdsLun</b> and 
    <b>IVdsLunPlex</b> interfaces to report hints currently applied 
    to a LUN or LUN plex, respectively.
    


     Hints are not directives to implementers. While implementers are in general expected to do their best to take hints into consideration, 
     they are not obligated to follow them. Implementers can opt for alternatives when unable to follow specified hints for
     technical reasons or when following them can result in a poor configuration.




## -see-also




<a href="https://msdn.microsoft.com/2582913a-bc13-45dc-b0c8-9429945014da">IVdsLun::ApplyHints</a>



<a href="https://msdn.microsoft.com/6cdbbf17-fcee-4cd4-bf5c-d994886262da">IVdsLun::QueryHints</a>



<a href="https://msdn.microsoft.com/66299644-4b70-4cd3-ae99-4d4084c3c3c5">IVdsLunPlex::ApplyHints</a>



<a href="https://msdn.microsoft.com/4ecb0840-8eaf-47c9-b8a9-98c738ed7daf">IVdsLunPlex::QueryHints</a>



<a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

