---
UID: NS:winioctl._FILE_SET_DEFECT_MGMT_BUFFER
title: FILE_SET_DEFECT_MGMT_BUFFER
description: Specifies the defect management state to be set.
helpviewer_keywords: ["*PFILE_SET_DEFECT_MGMT_BUFFER","FILE_SET_DEFECT_MGMT_BUFFER","FILE_SET_DEFECT_MGMT_BUFFER structure [Files]","PFILE_SET_DEFECT_MGMT_BUFFER","PFILE_SET_DEFECT_MGMT_BUFFER structure pointer [Files]","fs.file_set_defect_mgmt_buffer","winioctl/FILE_SET_DEFECT_MGMT_BUFFER","winioctl/PFILE_SET_DEFECT_MGMT_BUFFER"]
old-location: fs\file_set_defect_mgmt_buffer.htm
tech.root: fs
ms.assetid: 4a2ee2d5-8886-4472-85b7-de029eeffd55
ms.date: 12/05/2018
ms.keywords: '*PFILE_SET_DEFECT_MGMT_BUFFER, FILE_SET_DEFECT_MGMT_BUFFER, FILE_SET_DEFECT_MGMT_BUFFER structure [Files], PFILE_SET_DEFECT_MGMT_BUFFER, PFILE_SET_DEFECT_MGMT_BUFFER structure pointer [Files], fs.file_set_defect_mgmt_buffer, winioctl/FILE_SET_DEFECT_MGMT_BUFFER, winioctl/PFILE_SET_DEFECT_MGMT_BUFFER'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FILE_SET_DEFECT_MGMT_BUFFER, *PFILE_SET_DEFECT_MGMT_BUFFER
req.redist: 
f1_keywords:
 - _FILE_SET_DEFECT_MGMT_BUFFER
 - winioctl/_FILE_SET_DEFECT_MGMT_BUFFER
 - PFILE_SET_DEFECT_MGMT_BUFFER
 - winioctl/PFILE_SET_DEFECT_MGMT_BUFFER
 - FILE_SET_DEFECT_MGMT_BUFFER
 - winioctl/FILE_SET_DEFECT_MGMT_BUFFER
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
 - FILE_SET_DEFECT_MGMT_BUFFER
---

# FILE_SET_DEFECT_MGMT_BUFFER structure


## -description

Specifies the defect management state  to be set.

## -struct-fields

### -field Disable

If <b>TRUE</b>, indicates that defect management is disabled.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_defect_management">FSCTL_SET_DEFECT_MANAGEMENT</a>