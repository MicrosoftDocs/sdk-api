---
UID: NS:winioctl._CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT
title: "_CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT"
author: windows-sdk-content
description: Contains troubleshooting information about why a volume is in redirected mode.
old-location: fs\csv_query_veto_file_direct_io_output.htm
tech.root: fileio
ms.assetid: 1FEAB857-5C0E-4CD1-A72C-F8BD60AD24B4
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: "*PCSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT, CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT, CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT structure [Files], PCSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT, PCSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT structure pointer [Files], _CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT, fs.csv_query_veto_file_direct_io_output, winioctl/CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT, winioctl/PCSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT
product: Windows
targetos: Windows
req.typenames: CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT, *PCSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT
req.redist: 
---

# _CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT structure


## -description


Contains troubleshooting information about why a volume is in redirected mode.


## -struct-fields




### -field VetoedFromAltitudeIntegral

The integer portion of VetoedFromAltitude.


### -field VetoedFromAltitudeDecimal

The decimal portion of VetoedFromAltitude.


### -field Reason

The reason why volume is in a redirected mode.


## -remarks



CSV writes the troubleshooting strings to a diagnostic log that, when filtered, can provide hints as to why 
    a volume is in a redirected mode.




## -see-also




<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

