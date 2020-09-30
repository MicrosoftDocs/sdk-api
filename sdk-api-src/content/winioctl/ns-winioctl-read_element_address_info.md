---
UID: NS:winioctl._READ_ELEMENT_ADDRESS_INFO
title: READ_ELEMENT_ADDRESS_INFO
description: Represents the volume tag information. It is used by the IOCTL_CHANGER_QUERY_VOLUME_TAGS control code.
helpviewer_keywords: ["*PREAD_ELEMENT_ADDRESS_INFO","PREAD_ELEMENT_ADDRESS_INFO","PREAD_ELEMENT_ADDRESS_INFO structure pointer","READ_ELEMENT_ADDRESS_INFO","READ_ELEMENT_ADDRESS_INFO structure","_win32_read_element_address_info_str","base.read_element_address_info_str","winioctl/PREAD_ELEMENT_ADDRESS_INFO","winioctl/READ_ELEMENT_ADDRESS_INFO"]
old-location: base\read_element_address_info_str.htm
tech.root: base
ms.assetid: 2b7e611b-7db6-4ba6-ae1f-4269a96dbb16
ms.date: 12/05/2018
ms.keywords: '*PREAD_ELEMENT_ADDRESS_INFO, PREAD_ELEMENT_ADDRESS_INFO, PREAD_ELEMENT_ADDRESS_INFO structure pointer, READ_ELEMENT_ADDRESS_INFO, READ_ELEMENT_ADDRESS_INFO structure, _win32_read_element_address_info_str, base.read_element_address_info_str, winioctl/PREAD_ELEMENT_ADDRESS_INFO, winioctl/READ_ELEMENT_ADDRESS_INFO'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: READ_ELEMENT_ADDRESS_INFO, *PREAD_ELEMENT_ADDRESS_INFO
req.redist: 
f1_keywords:
 - _READ_ELEMENT_ADDRESS_INFO
 - winioctl/_READ_ELEMENT_ADDRESS_INFO
 - PREAD_ELEMENT_ADDRESS_INFO
 - winioctl/PREAD_ELEMENT_ADDRESS_INFO
 - READ_ELEMENT_ADDRESS_INFO
 - winioctl/READ_ELEMENT_ADDRESS_INFO
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
 - READ_ELEMENT_ADDRESS_INFO
---

# READ_ELEMENT_ADDRESS_INFO structure


## -description

Represents the volume tag information. It is used by the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_query_volume_tags">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a> control code.

## -struct-fields

### -field NumberOfElements

The number of elements matching criteria set forth by the <b>ActionCode</b> member of 
<a href="/windows/win32/api/winioctl/ns-winioctl-changer_send_volume_tag_information">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>. 




For information on compatibility with the current device, see the <b>Features0</b> member of 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a>.

### -field ElementStatus

An array of 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_status">CHANGER_ELEMENT_STATUS</a> structures, one for each element that corresponded with the information passed in with the 
<a href="/windows/win32/api/winioctl/ns-winioctl-changer_send_volume_tag_information">CHANGER_SEND_VOLUME_TAG_INFORMATION</a> structure.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_status">CHANGER_ELEMENT_STATUS</a>



<a href="/windows/win32/api/winioctl/ns-winioctl-changer_send_volume_tag_information">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_query_volume_tags">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a>