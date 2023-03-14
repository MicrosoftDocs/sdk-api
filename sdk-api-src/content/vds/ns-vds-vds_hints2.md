---
UID: NS:vds._VDS_HINTS2
title: VDS_HINTS2 (vds.h)
description: The VDS_HINTS2 structure (vds.h) contains the automagic hints for a LUN in a storage pool. 
helpviewer_keywords: ["*PVDS_HINTS2","PVDS_HINTS2","PVDS_HINTS2 structure pointer","VDS_HINTS2","VDS_HINTS2 structure","VDS_HINT_ALLOCATEHOTSPARE","VDS_HINT_BUSTYPE","VDS_HINT_CONSISTENCYCHECKENABLED","VDS_HINT_FASTCRASHRECOVERYREQUIRED","VDS_HINT_HARDWARECHECKSUMENABLED","VDS_HINT_ISYANKABLE","VDS_HINT_MEDIASCANENABLED","VDS_HINT_MOSTLYREADS","VDS_HINT_OPTIMIZEFORSEQUENTIALREADS","VDS_HINT_OPTIMIZEFORSEQUENTIALWRITES","VDS_HINT_READBACKVERIFYENABLED","VDS_HINT_READCACHINGENABLED","VDS_HINT_REMAPENABLED","VDS_HINT_USEMIRROREDCACHE","VDS_HINT_WRITECACHINGENABLED","VDS_HINT_WRITETHROUGHCACHINGENABLED","base.vds_hints2","vds/PVDS_HINTS2","vds/VDS_HINTS2","vdshwprv/PVDS_HINTS2","vdshwprv/VDS_HINTS2"]
old-location: base\vds_hints2.htm
tech.root: base
ms.assetid: e24935ac-17c8-4338-99cb-2408ca61da8a
ms.date: 08/05/2022
ms.keywords: '*PVDS_HINTS2, PVDS_HINTS2, PVDS_HINTS2 structure pointer, VDS_HINTS2, VDS_HINTS2 structure, VDS_HINT_ALLOCATEHOTSPARE, VDS_HINT_BUSTYPE, VDS_HINT_CONSISTENCYCHECKENABLED, VDS_HINT_FASTCRASHRECOVERYREQUIRED, VDS_HINT_HARDWARECHECKSUMENABLED, VDS_HINT_ISYANKABLE, VDS_HINT_MEDIASCANENABLED, VDS_HINT_MOSTLYREADS, VDS_HINT_OPTIMIZEFORSEQUENTIALREADS, VDS_HINT_OPTIMIZEFORSEQUENTIALWRITES, VDS_HINT_READBACKVERIFYENABLED, VDS_HINT_READCACHINGENABLED, VDS_HINT_REMAPENABLED, VDS_HINT_USEMIRROREDCACHE, VDS_HINT_WRITECACHINGENABLED, VDS_HINT_WRITETHROUGHCACHINGENABLED, base.vds_hints2, vds/PVDS_HINTS2, vds/VDS_HINTS2, vdshwprv/PVDS_HINTS2, vdshwprv/VDS_HINTS2'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_HINTS2, *PVDS_HINTS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_HINTS2
 - vds/_VDS_HINTS2
 - PVDS_HINTS2
 - vds/PVDS_HINTS2
 - VDS_HINTS2
 - vds/VDS_HINTS2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_HINTS2
---

# VDS_HINTS2 structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Contains the automagic hints for a LUN in a <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>.

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
The provider configures the LUN so that the drives that contribute to it can be physically removed with minimal system disruption. This is normally accomplished by ensuring that the LUN occupies as few drives as possible.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_ALLOCATEHOTSPARE"></a><a id="vds_hint_allocatehotspare"></a><dl>
<dt><b>VDS_HINT_ALLOCATEHOTSPARE</b></dt>
<dt>0x0000000000000200L</dt>
</dl>
</td>
<td width="60%">
The provider allocates a hot spare for the LUN. For more information, see <a href="/windows/desktop/VDS/hot-sparing">Hot Sparing</a>, <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_flag">VDS_DRIVE_FLAG</a>, and <a href="/windows/desktop/api/vds/ne-vds-vds_disk_flag">VDS_DISK_FLAG</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_BUSTYPE"></a><a id="vds_hint_bustype"></a><dl>
<dt><b>VDS_HINT_BUSTYPE</b></dt>
<dt>0x0000000000000400L</dt>
</dl>
</td>
<td width="60%">
The provider uses the specified bus type on the LUN. For more information, see <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_USEMIRROREDCACHE"></a><a id="vds_hint_usemirroredcache"></a><dl>
<dt><b>VDS_HINT_USEMIRROREDCACHE</b></dt>
<dt>0x0000000000000800L</dt>
</dl>
</td>
<td width="60%">
The provider uses a mirrored cache on the LUN. See the <b>VDS_SF_SUPPORTS_MIRRORED_CACHE</b>  value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_READCACHINGENABLED"></a><a id="vds_hint_readcachingenabled"></a><dl>
<dt><b>VDS_HINT_READCACHINGENABLED</b></dt>
<dt>0x0000000000001000L</dt>
</dl>
</td>
<td width="60%">
The provider enables read caching on the LUN. See the <b>VDS_LF_READ_CACHE_ENABLED</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_flag">VDS_LUN_FLAG</a>  enumeration and the <b>VDS_SF_READ_CACHING_CAPABLE</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_WRITECACHINGENABLED"></a><a id="vds_hint_writecachingenabled"></a><dl>
<dt><b>VDS_HINT_WRITECACHINGENABLED</b></dt>
<dt>0x0000000000002000L</dt>
</dl>
</td>
<td width="60%">
The provider enables write caching on the LUN. See the <b>VDS_LF_WRITE_CACHE_ENABLED</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_flag">VDS_LUN_FLAG</a>  enumeration and the <b>VDS_SF_WRITE_CACHING_CAPABLE</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_MEDIASCANENABLED"></a><a id="vds_hint_mediascanenabled"></a><dl>
<dt><b>VDS_HINT_MEDIASCANENABLED</b></dt>
<dt>0x0000000000004000L</dt>
</dl>
</td>
<td width="60%">
The provider enables media scanning on the LUN. See the <b>VDS_LF_MEDIA_SCAN_ENABLED</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_flag">VDS_LUN_FLAG</a>  enumeration and the <b>VDS_SF_MEDIA_SCAN_CAPABLE</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_HINT_CONSISTENCYCHECKENABLED"></a><a id="vds_hint_consistencycheckenabled"></a><dl>
<dt><b>VDS_HINT_CONSISTENCYCHECKENABLED</b></dt>
<dt>0x0000000000008000L</dt>
</dl>
</td>
<td width="60%">
The provider enables consistency checking on the LUN. See the <b>VDS_LF_CONSISTENCY_CHECK_ENABLED</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_flag">VDS_LUN_FLAG</a>  enumeration and the <b>VDS_SF_CONSISTENCY_CHECK_CAPABLE</b> value of the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_sub_system_flag">VDS_SUB_SYSTEM_FLAG</a> enumeration.

</td>
</tr>
</table>

### -field ullExpectedMaximumSize

The maximum size to which the LUN is expected to grow, in bytes. The value can be equal to, greater than, or 
      less than the value specified in the <i>ullSizeInBytes</i> parameter when the 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderstoragepools-createluninstoragepool">IVdsHwProviderStoragePools::CreateLunInStoragePool</a> method is called.
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

### -field ulReserved1

This member is reserved for future use. Do not use.

### -field ulReserved2

This member is reserved for future use. Do not use.

### -field ulReserved3

This member is reserved for future use. Do not use.

### -field bFastCrashRecoveryRequired

If this member is <b>TRUE</b>, the recovery time is limited. Set the <b>VDS_HINT_FASTCRASHRECOVERYREQUIRED</b> 
      flag in the <b>ullHintMask</b> member to indicate interest in this member.

### -field bMostlyReads

To optimize for a mostly-reads usage pattern (for example, through mirroring rather than parity striping), set 
      this member to <b>TRUE</b>. Otherwise, set it to <b>FALSE</b>. Set the <b>VDS_HINT_MOSTLYREADS</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.

### -field bOptimizeForSequentialReads

To optimize for a sequential-reads usage pattern, set this member to <b>TRUE</b>. Otherwise, set it to <b>FALSE</b>. Setting the 
      <b>bOptimizeForSequentialReads</b> and 
      <b>bOptimizeForSequentialWrites</b> members both to <b>FALSE</b> optimizes for random I/O. Set the 
      <b>VDS_HINT_OPTIMIZEFORSEQUENTIALREADS</b> flag in 
      the <b>ullHintMask</b> member to indicate interest in this member.

### -field bOptimizeForSequentialWrites

To optimize for a sequential-writes usage pattern, set this member to <b>TRUE</b>. Otherwise, set it to <b>FALSE</b>. Setting the 
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

If this member is <b>TRUE</b>, the provider verifies the writes to the LUN by readback. If it is <b>FALSE</b>, the provider does not verify writes. 
      Set the <b>VDS_HINT_READBACKVERIFYENABLED</b> flag in the 
      <b>ullHintMask</b> member to indicate interest in this member.

### -field bWriteThroughCachingEnabled

If this member is <b>TRUE</b>, the provider enables write-through caching on the LUN; if it is <b>FALSE</b>, the provider does not enable
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

### -field bAllocateHotSpare

<b>TRUE</b> if the client wants to allocate a hot spare drive for this LUN, or <b>FALSE</b> otherwise. Set the 
      <b>VDS_HINT_ALLOCATEHOTSPARE</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.

### -field bUseMirroredCache

<b>TRUE</b> if the client wants this LUN to use a mirrored cache, or <b>FALSE</b> otherwise. Set the 
      <b>VDS_HINT_USEMIRROREDCACHE</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.

### -field bReadCachingEnabled

<b>TRUE</b> if the client wants the LUN to use read caching, or <b>FALSE</b> otherwise. Set the 
      <b>VDS_HINT_READCACHINGENABLED</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.

### -field bWriteCachingEnabled

<b>TRUE</b> if the client wants the LUN to use write caching, or <b>FALSE</b> otherwise. Set the 
      <b>VDS_HINT_WRITECACHINGENABLED</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.

### -field bMediaScanEnabled

<b>TRUE</b> if the client wants to enable media scanning for this LUN, or <b>FALSE</b> otherwise. Set the 
      <b>VDS_HINT_MEDIASCANENABLED</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.

### -field bConsistencyCheckEnabled

<b>TRUE</b> if the client wants to enable consistency checking for this LUN, or <b>FALSE</b> otherwise. Set the 
      <b>VDS_HINT_CONSISTENCYCHECKENABLED</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.

### -field BusType

A 
      <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a> enumeration value that specifies the bus type for the LUN. Set the 
      <b>VDS_HINT_BUSTYPE</b> flag in the <b>ullHintMask</b> member to indicate 
      interest in this member.

### -field bReserved1

This member is reserved for future use. Do not use.

### -field bReserved2

This member is reserved for future use. Do not use.

### -field bReserved3

This member is reserved for future use. Do not use.

### -field sRebuildPriority

The rebuild priority for the LUN. The value can range from 0 (lowest priority) through 15 (highest priority).

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderstoragepools-createluninstoragepool">IVdsHwProviderStoragePools::CreateLunInStoragePool</a> method passes 
    this structure as a parameter to provide hints for creating a LUN in a storage pool. It is passed as a parameter in the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-applyhints2">IVdsLun2::ApplyHints2</a> method to apply a new set of hints to a 
    LUN. Further, it is returned by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-queryhints2">IVdsLun2::QueryHints2</a> method  to report hints currently applied 
    to a LUN or LUN plex, respectively.
    

Hints are not directives to implementers. While implementers are in general expected to do their best to take hints into consideration, 
     they are not obligated to follow them. Implementers can opt for alternatives when unable to follow specified hints for
     technical reasons or when following them can result in a poor configuration.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-applyhints2">IVdsLun2::ApplyHints2</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-queryhints2">IVdsLun2::QueryHints2</a>
