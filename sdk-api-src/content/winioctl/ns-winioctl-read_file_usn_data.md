---
UID: NS:winioctl.READ_FILE_USN_DATA
title: READ_FILE_USN_DATA
description: Specifies the versions of the update sequence number (USN) change journal supported by the application.
helpviewer_keywords: ["*PREAD_FILE_USN_DATA","PREAD_FILE_USN_DATA","PREAD_FILE_USN_DATA structure pointer [Files]","READ_FILE_USN_DATA","READ_FILE_USN_DATA structure [Files]","fs.read_file_usn_data","winioctl/PREAD_FILE_USN_DATA","winioctl/READ_FILE_USN_DATA"]
old-location: fs\read_file_usn_data.htm
tech.root: fs
ms.assetid: 8c403eec-7504-4a69-9f05-7a3a164557a6
ms.date: 12/05/2018
ms.keywords: '*PREAD_FILE_USN_DATA, PREAD_FILE_USN_DATA, PREAD_FILE_USN_DATA structure pointer [Files], READ_FILE_USN_DATA, READ_FILE_USN_DATA structure [Files], fs.read_file_usn_data, winioctl/PREAD_FILE_USN_DATA, winioctl/READ_FILE_USN_DATA'
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
targetos: Windows
req.typenames: READ_FILE_USN_DATA, *PREAD_FILE_USN_DATA
req.redist: 
f1_keywords:
 - PREAD_FILE_USN_DATA
 - winioctl/PREAD_FILE_USN_DATA
 - READ_FILE_USN_DATA
 - winioctl/READ_FILE_USN_DATA
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
 - READ_FILE_USN_DATA
---

# READ_FILE_USN_DATA structure


## -description

Specifies the versions of the update sequence number (USN) change journal supported by the 
    application. This structure is the input structure to the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_file_usn_data">FSCTL_READ_FILE_USN_DATA</a> control code.

## -struct-fields

### -field MinMajorVersion

The lowest version of the USN change journal accepted by the application. If the input buffer is not 
      specified this defaults to 2.

### -field MaxMajorVersion

The highest version of the USN change journal accepted by the application. If the input buffer is not 
      specified this defaults to 2. To support 128-bit file identifiers used by ReFS this must be 3 or higher.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>

