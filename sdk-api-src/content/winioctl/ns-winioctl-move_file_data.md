---
UID: NS:winioctl.MOVE_FILE_DATA
title: MOVE_FILE_DATA
author: windows-sdk-content
description: Contains input data for the FSCTL_MOVE_FILE control code.
old-location: fs\move_file_data_str.htm
old-project: FileIO
ms.assetid: 08bbeabc-b589-41b2-b3f2-70b2390f11f0
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PMOVE_FILE_DATA, MOVE_FILE_DATA, MOVE_FILE_DATA structure [Files], PMOVE_FILE_DATA, PMOVE_FILE_DATA structure pointer [Files], _win32_move_file_data_str, base.move_file_data_str, fs.move_file_data_str, winioctl/MOVE_FILE_DATA, winioctl/PMOVE_FILE_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MOVE_FILE_DATA, *PMOVE_FILE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - MOVE_FILE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# MOVE_FILE_DATA structure


## -description


Contains input data for the <a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a> 
    control code.


## -struct-fields




### -field FileHandle

A handle to the file to be moved.

To retrieve a handle to a file, use 
       <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.

If the file is encrypted, the handle must have the <b>FILE_READ_DATA</b>, 
       <b>FILE_WRITE_DATA</b>, <b>FILE_APPEND_DATA</b>, or 
       <b>FILE_EXECUTE</b> access right. For more information, see 
       <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -field StartingVcn

A VCN (cluster number relative to the beginning of a file) of the first cluster to be moved.


### -field StartingLcn

An LCN (cluster number on a volume) to which the VCN is to be moved.


### -field ClusterCount

The count of clusters to be moved.


## -remarks



To retrieve data to fill in this structure, use the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff545421">FSCTL_GET_RETRIEVAL_POINTERS</a> control 
    code.

The first cluster of a directory on a FAT file system volume cannot be moved.

When possible, move data in blocks aligned relative to each other in 16-kilobyte (KB) increments. This reduces copy-on-write overhead when shadow copies are enabled, because shadow copy space is  increased and performance is reduced when the following conditions occur:

<ul>
<li>The move request block size is less than or equal to 16 KB.</li>
<li>The move delta is not in increments of 16 KB.</li>
</ul>
The move delta is the number of bytes between the start of the source block and the start of the target block. In other words, a block starting at offset X (on-disk) can be moved to a starting offset Y if the absolute value of X minus Y is an even multiple of 16 KB. So, assuming 4-KB clusters, a move from cluster 3 to cluster 27 will be optimized,  but a move from cluster 18 to cluster 24 will not.  Note that mod(3,4) = 3 = mod(27,4).  Mod 4 is chosen because four clusters at 4 KB each is equivalent to 16 KB.  Therefore, a volume formatted to a 16-KB cluster size will result in all move files being optimized.

For more information about shadow copies, see <a href="https://msdn.microsoft.com/654c67e8-2f17-4d93-aabd-fabd71c4c852">Volume Shadow Copy Service</a>.




## -see-also




<a href="https://msdn.microsoft.com/27ccaab7-ec89-489b-80dc-df9beb7969bc">Defragmenting Files</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545421">FSCTL_GET_RETRIEVAL_POINTERS</a>



<a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a>



<a href="https://msdn.microsoft.com/d026ee3a-c165-42a2-a4e1-efccdafbefc5">GetFileInformationByHandle</a>
 

 

