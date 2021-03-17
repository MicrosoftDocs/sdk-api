---
UID: NS:winioctl._GET_LENGTH_INFORMATION
title: GET_LENGTH_INFORMATION
description: Contains disk, volume, or partition length information used by the IOCTL_DISK_GET_LENGTH_INFO control code.
helpviewer_keywords: ["*PGET_LENGTH_INFORMATION","GET_LENGTH_INFORMATION","GET_LENGTH_INFORMATION structure [Files]","_win32_get_length_information_str","base.get_length_information_str","fs.get_length_information_str","winioctl/GET_LENGTH_INFORMATION"]
old-location: fs\get_length_information_str.htm
tech.root: fs
ms.assetid: a0d2a5bc-32e0-47d6-a4f0-84bd7f6bb746
ms.date: 12/05/2018
ms.keywords: '*PGET_LENGTH_INFORMATION, GET_LENGTH_INFORMATION, GET_LENGTH_INFORMATION structure [Files], _win32_get_length_information_str, base.get_length_information_str, fs.get_length_information_str, winioctl/GET_LENGTH_INFORMATION'
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
req.typenames: GET_LENGTH_INFORMATION, *PGET_LENGTH_INFORMATION
req.redist: 
f1_keywords:
 - _GET_LENGTH_INFORMATION
 - winioctl/_GET_LENGTH_INFORMATION
 - PGET_LENGTH_INFORMATION
 - winioctl/PGET_LENGTH_INFORMATION
 - GET_LENGTH_INFORMATION
 - winioctl/GET_LENGTH_INFORMATION
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
 - GET_LENGTH_INFORMATION
---

# GET_LENGTH_INFORMATION structure


## -description

Contains disk, volume, or partition length information used by the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_length_info">IOCTL_DISK_GET_LENGTH_INFO</a> control code.

## -struct-fields

### -field Length

The length of the disk, volume, or partition, in bytes.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_length_info">IOCTL_DISK_GET_LENGTH_INFO</a>