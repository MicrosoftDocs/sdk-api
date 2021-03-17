---
UID: NS:virtdisk._MERGE_VIRTUAL_DISK_PARAMETERS
title: MERGE_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains virtual hard disk (VHD) merge request parameters.
helpviewer_keywords: ["*PMERGE_VIRTUAL_DISK_PARAMETERS","MERGE_VIRTUAL_DISK_PARAMETERS","MERGE_VIRTUAL_DISK_PARAMETERS structure [VHD]","PMERGE_VIRTUAL_DISK_PARAMETERS","PMERGE_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","_MERGE_VIRTUAL_DISK_PARAMETERS","vdssys/MERGE_VIRTUAL_DISK_PARAMETERS","vdssys/PMERGE_VIRTUAL_DISK_PARAMETERS","vhd.merge_virtual_disk_parameters","virtdisk/MERGE_VIRTUAL_DISK_PARAMETERS","virtdisk/PMERGE_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\merge_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 5bb84e11-677d-42f5-b5b6-59f23b9a8ab7
ms.date: 12/05/2018
ms.keywords: '*PMERGE_VIRTUAL_DISK_PARAMETERS, MERGE_VIRTUAL_DISK_PARAMETERS, MERGE_VIRTUAL_DISK_PARAMETERS structure [VHD], PMERGE_VIRTUAL_DISK_PARAMETERS, PMERGE_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _MERGE_VIRTUAL_DISK_PARAMETERS, vdssys/MERGE_VIRTUAL_DISK_PARAMETERS, vdssys/PMERGE_VIRTUAL_DISK_PARAMETERS, vhd.merge_virtual_disk_parameters, virtdisk/MERGE_VIRTUAL_DISK_PARAMETERS, virtdisk/PMERGE_VIRTUAL_DISK_PARAMETERS'
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: MERGE_VIRTUAL_DISK_PARAMETERS, *PMERGE_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MERGE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_MERGE_VIRTUAL_DISK_PARAMETERS
 - PMERGE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PMERGE_VIRTUAL_DISK_PARAMETERS
 - MERGE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/MERGE_VIRTUAL_DISK_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - MERGE_VIRTUAL_DISK_PARAMETERS
---

# MERGE_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains virtual hard disk (VHD) merge request parameters.

## -struct-fields

### -field Version

A <a href="/windows/win32/api/virtdisk/ne-virtdisk-merge_virtual_disk_version">MERGE_VIRTUAL_DISK_VERSION</a> enumeration 
      that specifies the version of the 
      <b>MERGE_VIRTUAL_DISK_PARAMETERS</b> structure 
      being passed to or from the VHD functions.

### -field Version1

This structure is used when the Version member is <b>MERGE_VIRTUAL_DISK_VERSION_1</b> 
       (1).

### -field Version1.MergeDepth

Depth of the merge request. This is the number of parent disks in the differencing chain to merge 
         together.

<div class="alert"><b>Note</b>  The RWDepth of the virtual disk must be greater than <b>MergeDepth</b>. For more 
         information, see 
         <a href="/windows/win32/api/virtdisk/ns-virtdisk-open_virtual_disk_parameters">OPEN_VIRTUAL_DISK_PARAMETERS</a>.</div>
<div> </div>

### -field Version2

This structure is used when the Version member is <b>MERGE_VIRTUAL_DISK_VERSION_2</b> 
        (2).

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported until Windows 8 and Windows Server 2012.

### -field Version2.MergeSourceDepth

Depth from the leaf from which to begin the merge.  The leaf is at depth 1.

### -field Version2.MergeTargetDepth

Depth from  the leaf to target the merge.  The leaf is at depth 1.

## -remarks

The depth of a merge request specified by the <b>MergeDepth</b> member is the number of  
    parent VHD image files in the differencing chain to be merged.  For more information, see 
    <a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk">MergeVirtualDisk</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk">MergeVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>