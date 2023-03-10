---
UID: NS:winioctl._CHANGER_INITIALIZE_ELEMENT_STATUS
title: CHANGER_INITIALIZE_ELEMENT_STATUS
description: Represents the status of all media changer elements or the specified elements of a particular type.
helpviewer_keywords: ["*PCHANGER_INITIALIZE_ELEMENT_STATUS","CHANGER_INITIALIZE_ELEMENT_STATUS","CHANGER_INITIALIZE_ELEMENT_STATUS structure","PCHANGER_INITIALIZE_ELEMENT_STATUS","PCHANGER_INITIALIZE_ELEMENT_STATUS structure pointer","_win32_changer_initialize_element_status_str","base.changer_initialize_element_status_str","winioctl/CHANGER_INITIALIZE_ELEMENT_STATUS","winioctl/PCHANGER_INITIALIZE_ELEMENT_STATUS"]
old-location: base\changer_initialize_element_status_str.htm
tech.root: base
ms.assetid: 593df7e3-dd2b-4ba9-b7a0-ed6ea06586ba
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_INITIALIZE_ELEMENT_STATUS, CHANGER_INITIALIZE_ELEMENT_STATUS, CHANGER_INITIALIZE_ELEMENT_STATUS structure, PCHANGER_INITIALIZE_ELEMENT_STATUS, PCHANGER_INITIALIZE_ELEMENT_STATUS structure pointer, _win32_changer_initialize_element_status_str, base.changer_initialize_element_status_str, winioctl/CHANGER_INITIALIZE_ELEMENT_STATUS, winioctl/PCHANGER_INITIALIZE_ELEMENT_STATUS'
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
req.typenames: CHANGER_INITIALIZE_ELEMENT_STATUS, *PCHANGER_INITIALIZE_ELEMENT_STATUS
req.redist: 
f1_keywords:
 - _CHANGER_INITIALIZE_ELEMENT_STATUS
 - winioctl/_CHANGER_INITIALIZE_ELEMENT_STATUS
 - PCHANGER_INITIALIZE_ELEMENT_STATUS
 - winioctl/PCHANGER_INITIALIZE_ELEMENT_STATUS
 - CHANGER_INITIALIZE_ELEMENT_STATUS
 - winioctl/CHANGER_INITIALIZE_ELEMENT_STATUS
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
 - CHANGER_INITIALIZE_ELEMENT_STATUS
---

# CHANGER_INITIALIZE_ELEMENT_STATUS structure


## -description

Represents the status of all media changer elements or the specified elements of a particular type.

## -struct-fields

### -field ElementList

A 
<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a> structure that lists the elements and range on which to initialize. 




If CHANGER_INIT_ELEM_STAT_WITH_RANGE is set in the <b>Features0</b> member of 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a>, the changer supports initializing a range of elements. In this case, the <b>ElementType</b> member can be one of the following: ChangerTransport, ChangerSlot, ChangerDrive, or ChangerIEPort. Otherwise, the element type must be AllElements and the <b>NumberOfElements</b> member is ignored.

### -field BarCodeScan

If this member is <b>TRUE</b>, a bar-code scan should be used. Otherwise, it should not. If the changer has nonvolatile RAM, using a bar-code scan is an optimization. 




This member is applicable only if CHANGER_BAR_CODE_SCANNER_INSTALLED is set in the <b>Features0</b> member of 
<a href="/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_initialize_element_status">IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS</a>