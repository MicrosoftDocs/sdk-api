---
UID: NS:winioctl._CSV_IS_OWNED_BY_CSVFS
title: CSV_IS_OWNED_BY_CSVFS

description: Contains the output for the FSCTL_IS_VOLUME_OWNED_BYCSVFS control code that determines whether a volume is owned by CSVFS.
old-location: fs\csv_is_owned_by_csvfs.htm
tech.root: FileIO
ms.assetid: F189E0F9-F711-4AB6-8237-775855FCD290

ms.date: 12/05/2018
ms.keywords: "*PCSV_IS_OWNED_BY_CSVFS, CSV_IS_OWNED_BY_CSVFS, CSV_IS_OWNED_BY_CSVFS structure [Files], PCSV_IS_OWNED_BY_CSVFS, PCSV_IS_OWNED_BY_CSVFS structure pointer [Files], fs.csv_is_owned_by_csvfs, winioctl/CSV_IS_OWNED_BY_CSVFS, winioctl/PCSV_IS_OWNED_BY_CSVFS"
ms.topic: struct
f1_keywords: 
 - "winioctl/CSV_IS_OWNED_BY_CSVFS"
dev_langs:
 - c++
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
 - CSV_IS_OWNED_BY_CSVFS
targetos: Windows
req.typenames: CSV_IS_OWNED_BY_CSVFS, *PCSV_IS_OWNED_BY_CSVFS
req.redist: 
---

# CSV_IS_OWNED_BY_CSVFS structure


## -description


Contains the output for the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_is_volume_owned_bycsvfs">FSCTL_IS_VOLUME_OWNED_BYCSVFS</a> control code 
    that determines whether a volume is owned by CSVFS.


## -struct-fields




### -field OwnedByCSVFS

<b>TRUE</b> if a volume is owned by CSVFS; otherwise, 
      <b>FALSE</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_is_volume_owned_bycsvfs">FSCTL_IS_VOLUME_OWNED_BYCSVFS</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>
 

 

