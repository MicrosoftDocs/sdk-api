---
UID: NS:winioctl._CHANGER_READ_ELEMENT_STATUS
title: CHANGER_READ_ELEMENT_STATUS
description: Contains information that the IOCTL_CHANGER_GET_ELEMENT_STATUS control code needs to determine the elements whose status is to be retrieved.
helpviewer_keywords: ["*PCHANGER_READ_ELEMENT_STATUS","CHANGER_READ_ELEMENT_STATUS","CHANGER_READ_ELEMENT_STATUS structure","PCHANGER_READ_ELEMENT_STATUS","PCHANGER_READ_ELEMENT_STATUS structure pointer","_win32_changer_read_element_status_str","base.changer_read_element_status_str","winioctl/CHANGER_READ_ELEMENT_STATUS","winioctl/PCHANGER_READ_ELEMENT_STATUS"]
old-location: base\changer_read_element_status_str.htm
tech.root: base
ms.assetid: 4eefc457-ba39-4025-98c8-21f599a87fcb
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_READ_ELEMENT_STATUS, CHANGER_READ_ELEMENT_STATUS, CHANGER_READ_ELEMENT_STATUS structure, PCHANGER_READ_ELEMENT_STATUS, PCHANGER_READ_ELEMENT_STATUS structure pointer, _win32_changer_read_element_status_str, base.changer_read_element_status_str, winioctl/CHANGER_READ_ELEMENT_STATUS, winioctl/PCHANGER_READ_ELEMENT_STATUS'
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
req.typenames: CHANGER_READ_ELEMENT_STATUS, *PCHANGER_READ_ELEMENT_STATUS
req.redist: 
f1_keywords:
 - _CHANGER_READ_ELEMENT_STATUS
 - winioctl/_CHANGER_READ_ELEMENT_STATUS
 - PCHANGER_READ_ELEMENT_STATUS
 - winioctl/PCHANGER_READ_ELEMENT_STATUS
 - CHANGER_READ_ELEMENT_STATUS
 - winioctl/CHANGER_READ_ELEMENT_STATUS
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
 - CHANGER_READ_ELEMENT_STATUS
---

# CHANGER_READ_ELEMENT_STATUS structure


## -description

Contains information that the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_get_element_status">IOCTL_CHANGER_GET_ELEMENT_STATUS</a> control code needs to determine the elements whose status is to be retrieved.

## -struct-fields

### -field ElementList

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a> structure that contains an array of structures that represents the range of elements for which information is to be retrieved. The <b>ElementType</b> member of each structure can be one of the following values: ChangerDrive, ChangerSlot, ChangerTransport, ChangerIEPort, or AllElements.

### -field VolumeTagInfo

If this member is <b>TRUE</b>, volume tag information is to be retrieved. Otherwise, no volume information is retrieved. A volume tag can be a bar code or an application-defined value. This member is valid only if the <b>Features0</b> member of the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a> structure is CHANGER_BAR_CODE_SCANNER_INSTALLED or CHANGER_VOLUME_IDENTIFICATION.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_get_element_status">IOCTL_CHANGER_GET_ELEMENT_STATUS</a>