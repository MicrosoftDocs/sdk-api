---
UID: NS:winioctl._CHANGER_INITIALIZE_ELEMENT_STATUS
title: CHANGER_INITIALIZE_ELEMENT_STATUS
author: windows-sdk-content
description: Represents the status of all media changer elements or the specified elements of a particular type.
old-location: base\changer_initialize_element_status_str.htm
tech.root: devio
ms.assetid: 593df7e3-dd2b-4ba9-b7a0-ed6ea06586ba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_INITIALIZE_ELEMENT_STATUS, CHANGER_INITIALIZE_ELEMENT_STATUS, CHANGER_INITIALIZE_ELEMENT_STATUS structure, PCHANGER_INITIALIZE_ELEMENT_STATUS, PCHANGER_INITIALIZE_ELEMENT_STATUS structure pointer, _win32_changer_initialize_element_status_str, base.changer_initialize_element_status_str, winioctl/CHANGER_INITIALIZE_ELEMENT_STATUS, winioctl/PCHANGER_INITIALIZE_ELEMENT_STATUS'
ms.topic: struct
f1_keywords:
- winioctl/CHANGER_INITIALIZE_ELEMENT_STATUS
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- CHANGER_INITIALIZE_ELEMENT_STATUS
targetos: Windows
req.typenames: CHANGER_INITIALIZE_ELEMENT_STATUS, *PCHANGER_INITIALIZE_ELEMENT_STATUS
req.redist: 
---

# CHANGER_INITIALIZE_ELEMENT_STATUS structure


## -description


Represents the status of all media changer elements or the specified elements of a particular type.


## -struct-fields




### -field ElementList

A 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a> structure that lists the elements and range on which to initialize. 




If CHANGER_INIT_ELEM_STAT_WITH_RANGE is set in the <b>Features0</b> member of 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a>, the changer supports initializing a range of elements. In this case, the <b>ElementType</b> member can be one of the following: ChangerTransport, ChangerSlot, ChangerDrive, or ChangerIEPort. Otherwise, the element type must be AllElements and the <b>NumberOfElements</b> member is ignored.


### -field BarCodeScan

If this member is <b>TRUE</b>, a bar-code scan should be used. Otherwise, it should not. If the changer has nonvolatile RAM, using a bar-code scan is an optimization. 




This member is applicable only if CHANGER_BAR_CODE_SCANNER_INSTALLED is set in the <b>Features0</b> member of 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-get_changer_parameters">GET_CHANGER_PARAMETERS</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_initialize_element_status">IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS</a>
 

 

