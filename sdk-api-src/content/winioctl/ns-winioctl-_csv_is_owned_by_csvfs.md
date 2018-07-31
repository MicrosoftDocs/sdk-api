---
UID: NS:winioctl._CSV_IS_OWNED_BY_CSVFS
title: "_CSV_IS_OWNED_BY_CSVFS"
author: windows-sdk-content
description: Contains the output for the FSCTL_IS_VOLUME_OWNED_BYCSVFS control code that determines whether a volume is owned by CSVFS.
old-location: fs\csv_is_owned_by_csvfs.htm
old-project: FileIO
ms.assetid: F189E0F9-F711-4AB6-8237-775855FCD290
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PCSV_IS_OWNED_BY_CSVFS, CSV_IS_OWNED_BY_CSVFS, CSV_IS_OWNED_BY_CSVFS structure [Files], PCSV_IS_OWNED_BY_CSVFS, PCSV_IS_OWNED_BY_CSVFS structure pointer [Files], _CSV_IS_OWNED_BY_CSVFS, fs.csv_is_owned_by_csvfs, winioctl/CSV_IS_OWNED_BY_CSVFS, winioctl/PCSV_IS_OWNED_BY_CSVFS"
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
tech.root: 
req.typenames: CSV_IS_OWNED_BY_CSVFS, *PCSV_IS_OWNED_BY_CSVFS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CSV_IS_OWNED_BY_CSVFS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CSV_IS_OWNED_BY_CSVFS structure


## -description


Contains the output for the 
    <a href="https://msdn.microsoft.com/AA9D31DD-352C-4509-A5F3-55DC1C685E33">FSCTL_IS_VOLUME_OWNED_BYCSVFS</a> control code 
    that determines whether a volume is owned by CSVFS.


## -struct-fields




### -field OwnedByCSVFS

<b>TRUE</b> if a volume is owned by CSVFS; otherwise, 
      <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/AA9D31DD-352C-4509-A5F3-55DC1C685E33">FSCTL_IS_VOLUME_OWNED_BYCSVFS</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

