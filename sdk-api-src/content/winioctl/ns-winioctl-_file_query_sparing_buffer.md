---
UID: NS:winioctl._FILE_QUERY_SPARING_BUFFER
title: "_FILE_QUERY_SPARING_BUFFER"
author: windows-sdk-content
description: Contains defect management properties.
old-location: fs\file_query_sparing_buffer.htm
old-project: FileIO
ms.assetid: 4b9b44ec-9e8e-4ebd-b192-952bbb71005d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PFILE_QUERY_SPARING_BUFFER, FILE_QUERY_SPARING_BUFFER, FILE_QUERY_SPARING_BUFFER structure [Files], PFILE_QUERY_SPARING_BUFFER, PFILE_QUERY_SPARING_BUFFER structure pointer [Files], _FILE_QUERY_SPARING_BUFFER, fs.file_query_sparing_buffer, winioctl/FILE_QUERY_SPARING_BUFFER, winioctl/PFILE_QUERY_SPARING_BUFFER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: FILE_QUERY_SPARING_BUFFER, *PFILE_QUERY_SPARING_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	FILE_QUERY_SPARING_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_QUERY_SPARING_BUFFER structure


## -description


Contains   defect management properties.


## -struct-fields




### -field SparingUnitBytes

The size of a sparing packet and the underlying error check and correction (ECC) block size of the volume.


### -field SoftwareSparing

If <b>TRUE</b>, indicates that sparing behavior is software-based; if <b>FALSE</b>, it is hardware-based.


### -field TotalSpareBlocks

The total number of blocks allocated for sparing.


### -field FreeSpareBlocks

The  number of blocks available for sparing.


## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/72122388-a42f-4c67-9539-20eb4c59dcf0">FSCTL_QUERY_SPARING_INFO</a>
 

 

