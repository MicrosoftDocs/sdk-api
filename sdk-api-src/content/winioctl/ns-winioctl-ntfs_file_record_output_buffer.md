---
UID: NS:winioctl.NTFS_FILE_RECORD_OUTPUT_BUFFER
title: NTFS_FILE_RECORD_OUTPUT_BUFFER
author: windows-sdk-content
description: Receives output data from the FSCTL_GET_NTFS_FILE_RECORD control code.
old-location: fs\ntfs_file_record_output_buffer_str.htm
old-project: FileIO
ms.assetid: e2597939-5159-4c35-9a1f-f3be43081d72
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PNTFS_FILE_RECORD_OUTPUT_BUFFER, NTFS_FILE_RECORD_OUTPUT_BUFFER, NTFS_FILE_RECORD_OUTPUT_BUFFER structure [Files], PNTFS_FILE_RECORD_OUTPUT_BUFFER, PNTFS_FILE_RECORD_OUTPUT_BUFFER structure pointer [Files], _win32_ntfs_file_record_output_buffer_str, base.ntfs_file_record_output_buffer_str, fs.ntfs_file_record_output_buffer_str, winioctl/NTFS_FILE_RECORD_OUTPUT_BUFFER, winioctl/PNTFS_FILE_RECORD_OUTPUT_BUFFER"
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
req.typenames: NTFS_FILE_RECORD_OUTPUT_BUFFER, *PNTFS_FILE_RECORD_OUTPUT_BUFFER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - NTFS_FILE_RECORD_OUTPUT_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# NTFS_FILE_RECORD_OUTPUT_BUFFER structure


## -description


Receives output data from the 
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> control code.


## -struct-fields




### -field FileReferenceNumber

The file identifier of the returned file record. This is not necessarily the file identifier specified in the <b>FileReferenceNumber</b> member of the 
<a href="https://msdn.microsoft.com/8b0317ca-6d0e-4a04-a05a-1627d22171e3">NTFS_FILE_RECORD_INPUT_BUFFER</a> structure. Refer to the Remarks section of the reference page for 
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> for more information.


### -field FileRecordLength

The length of the returned file record, in bytes.


### -field FileRecordBuffer

The starting location of the buffer for the returned file record.


## -remarks



To retrieve data to fill in this structure, use the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> control code.




## -see-also




<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a>



<a href="https://msdn.microsoft.com/8b0317ca-6d0e-4a04-a05a-1627d22171e3">NTFS_FILE_RECORD_INPUT_BUFFER</a>
 

 

