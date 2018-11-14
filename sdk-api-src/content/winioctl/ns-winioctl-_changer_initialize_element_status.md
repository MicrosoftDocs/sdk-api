---
UID: NS:winioctl._CHANGER_INITIALIZE_ELEMENT_STATUS
title: "_CHANGER_INITIALIZE_ELEMENT_STATUS"
author: windows-sdk-content
description: Represents the status of all media changer elements or the specified elements of a particular type.
old-location: base\changer_initialize_element_status_str.htm
tech.root: devio
ms.assetid: 593df7e3-dd2b-4ba9-b7a0-ed6ea06586ba
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: "*PCHANGER_INITIALIZE_ELEMENT_STATUS, CHANGER_INITIALIZE_ELEMENT_STATUS, CHANGER_INITIALIZE_ELEMENT_STATUS structure, PCHANGER_INITIALIZE_ELEMENT_STATUS, PCHANGER_INITIALIZE_ELEMENT_STATUS structure pointer, _CHANGER_INITIALIZE_ELEMENT_STATUS, _win32_changer_initialize_element_status_str, base.changer_initialize_element_status_str, winioctl/CHANGER_INITIALIZE_ELEMENT_STATUS, winioctl/PCHANGER_INITIALIZE_ELEMENT_STATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: CHANGER_INITIALIZE_ELEMENT_STATUS, *PCHANGER_INITIALIZE_ELEMENT_STATUS
req.redist: 
---

# _CHANGER_INITIALIZE_ELEMENT_STATUS structure


## -description


Represents the status of all media changer elements or the specified elements of a particular type.


## -struct-fields




### -field ElementList

A 
<a href="https://msdn.microsoft.com/cb1fcf78-b36a-4551-8eeb-da58edc80890">CHANGER_ELEMENT_LIST</a> structure that lists the elements and range on which to initialize. 




If CHANGER_INIT_ELEM_STAT_WITH_RANGE is set in the <b>Features0</b> member of 
<a href="https://msdn.microsoft.com/ad5b6cc3-19f1-4196-9f03-791f342d0cf9">GET_CHANGER_PARAMETERS</a>, the changer supports initializing a range of elements. In this case, the <b>ElementType</b> member can be one of the following: ChangerTransport, ChangerSlot, ChangerDrive, or ChangerIEPort. Otherwise, the element type must be AllElements and the <b>NumberOfElements</b> member is ignored.


### -field BarCodeScan

If this member is <b>TRUE</b>, a bar-code scan should be used. Otherwise, it should not. If the changer has nonvolatile RAM, using a bar-code scan is an optimization. 




This member is applicable only if CHANGER_BAR_CODE_SCANNER_INSTALLED is set in the <b>Features0</b> member of 
<a href="https://msdn.microsoft.com/ad5b6cc3-19f1-4196-9f03-791f342d0cf9">GET_CHANGER_PARAMETERS</a>.


## -see-also




<a href="https://msdn.microsoft.com/cb1fcf78-b36a-4551-8eeb-da58edc80890">CHANGER_ELEMENT_LIST</a>



<a href="https://msdn.microsoft.com/be054a22-cde4-4efd-bd66-eb67b007fd19">IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS</a>
 

 

