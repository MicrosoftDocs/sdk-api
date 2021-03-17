---
UID: NS:winioctl._DISK_CACHE_INFORMATION
title: DISK_CACHE_INFORMATION
description: Provides information about the disk cache.
helpviewer_keywords: ["*PDISK_CACHE_INFORMATION","DISK_CACHE_INFORMATION","DISK_CACHE_INFORMATION structure [Files]","EqualPriority","KeepPrefetchedData","KeepReadData","PDISK_CACHE_INFORMATION","PDISK_CACHE_INFORMATION structure pointer [Files]","base.disk_cache_information_str","fs.disk_cache_information_str","winioctl/DISK_CACHE_INFORMATION","winioctl/PDISK_CACHE_INFORMATION"]
old-location: fs\disk_cache_information_str.htm
tech.root: fs
ms.assetid: ea175bea-5f2b-4f3e-9fe0-239b1d2e3d96
ms.date: 12/05/2018
ms.keywords: '*PDISK_CACHE_INFORMATION, DISK_CACHE_INFORMATION, DISK_CACHE_INFORMATION structure [Files], EqualPriority, KeepPrefetchedData, KeepReadData, PDISK_CACHE_INFORMATION, PDISK_CACHE_INFORMATION structure pointer [Files], base.disk_cache_information_str, fs.disk_cache_information_str, winioctl/DISK_CACHE_INFORMATION, winioctl/PDISK_CACHE_INFORMATION'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: DISK_CACHE_INFORMATION, *PDISK_CACHE_INFORMATION
req.redist: 
f1_keywords:
 - _DISK_CACHE_INFORMATION
 - winioctl/_DISK_CACHE_INFORMATION
 - PDISK_CACHE_INFORMATION
 - winioctl/PDISK_CACHE_INFORMATION
 - DISK_CACHE_INFORMATION
 - winioctl/DISK_CACHE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DISK_CACHE_INFORMATION
---

# DISK_CACHE_INFORMATION structure


## -description

Provides information about the disk cache.This structure is used by the <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_cache_information">IOCTL_DISK_GET_CACHE_INFORMATION</a> and <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_cache_information">IOCTL_DISK_SET_CACHE_INFORMATION</a> control codes.

## -struct-fields

### -field ParametersSavable

Indicates whether the device is capable of saving any parameters in nonvolatile storage.

### -field ReadCacheEnabled

Indicates whether the read cache is enabled.

### -field WriteCacheEnabled

Indicates whether the write cache is enabled.

### -field ReadRetentionPriority

Determines the likelihood of data cached from a read operation remaining in the cache. This data might be given a different priority than data cached under other circumstances, such as from a prefetch operation.

 This member can be one of the following values from the <b>DISK_CACHE_RETENTION_PRIORITY</b> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EqualPriority"></a><a id="equalpriority"></a><a id="EQUALPRIORITY"></a><dl>
<dt><b>EqualPriority</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No data is held in the cache on a preferential basis.

</td>
</tr>
<tr>
<td width="40%"><a id="KeepPrefetchedData"></a><a id="keepprefetcheddata"></a><a id="KEEPPREFETCHEDDATA"></a><dl>
<dt><b>KeepPrefetchedData</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A preference is to be given to prefetched data.

</td>
</tr>
<tr>
<td width="40%"><a id="KeepReadData"></a><a id="keepreaddata"></a><a id="KEEPREADDATA"></a><dl>
<dt><b>KeepReadData</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A preference is to be given to data cached from a read operation.

</td>
</tr>
</table>

### -field WriteRetentionPriority

Determines the likelihood of data cached from a write operation remaining in the cache. This data might be given a different priority than data cached under other circumstances, such as from a prefetch operation.

### -field DisablePrefetchTransferLength

Disables prefetching. Prefetching might be disabled whenever the number of blocks requested exceeds the value in <i>DisablePrefetchTransferLength</i>. When zero, prefetching is disabled no matter what the size of the block request.

### -field PrefetchScalar

If this member is  <b>TRUE</b>,  the union is a <b>ScalarPrefetch</b> structure. Otherwise, the union is a <b>BlockPrefetch</b> structure.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.ScalarPrefetch

### -field DUMMYUNIONNAME.ScalarPrefetch.Minimum

The scalar multiplier of the transfer length of the request. This member is valid  only when <b>PrefetchScalar</b> is <b>TRUE</b>. When <b>PrefetchScalar</b> is <b>TRUE</b>, this value  is multiplied by the transfer length to obtain the minimum amount of data that can be prefetched into the cache on a disk operation.

### -field DUMMYUNIONNAME.ScalarPrefetch.Maximum

The scalar multiplier of the transfer length of the request. This member is valid only when <b>PrefetchScalar</b> is <b>TRUE</b>. When <b>PrefetchScalar</b> is <b>TRUE</b>, this value  is multiplied by the transfer length to obtain the maximum amount of data that can be prefetched into the cache on a disk operation.

### -field DUMMYUNIONNAME.ScalarPrefetch.MaximumBlocks

The maximum number of blocks which can be prefetched.

### -field DUMMYUNIONNAME.BlockPrefetch

### -field DUMMYUNIONNAME.BlockPrefetch.Minimum

The minimum amount of data that can be prefetched into the cache on a disk operation, as an absolute number of disk blocks. This member is valid only when <b>PrefetchScalar</b> is <b>FALSE</b>.

### -field DUMMYUNIONNAME.BlockPrefetch.Maximum

The maximum amount of data  that can be prefetched into the cache on a disk operation, as an absolute number of disk blocks. This member is valid only when <b>PrefetchScalar</b> is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_cache_information">IOCTL_DISK_GET_CACHE_INFORMATION</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_cache_information">IOCTL_DISK_SET_CACHE_INFORMATION</a>