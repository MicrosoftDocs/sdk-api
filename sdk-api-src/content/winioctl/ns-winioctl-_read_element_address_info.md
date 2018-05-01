---
UID: NS:winioctl._READ_ELEMENT_ADDRESS_INFO
title: "_READ_ELEMENT_ADDRESS_INFO"
author: windows-driver-content
description: Represents the volume tag information. It is used by the IOCTL_CHANGER_QUERY_VOLUME_TAGS control code.
old-location: base\read_element_address_info_str.htm
old-project: DevIO
ms.assetid: 2b7e611b-7db6-4ba6-ae1f-4269a96dbb16
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: "*PREAD_ELEMENT_ADDRESS_INFO, PREAD_ELEMENT_ADDRESS_INFO, PREAD_ELEMENT_ADDRESS_INFO structure pointer, READ_ELEMENT_ADDRESS_INFO, READ_ELEMENT_ADDRESS_INFO structure, _READ_ELEMENT_ADDRESS_INFO, _win32_read_element_address_info_str, base.read_element_address_info_str, winioctl/PREAD_ELEMENT_ADDRESS_INFO, winioctl/READ_ELEMENT_ADDRESS_INFO"
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
req.typenames: READ_ELEMENT_ADDRESS_INFO, *PREAD_ELEMENT_ADDRESS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	READ_ELEMENT_ADDRESS_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _READ_ELEMENT_ADDRESS_INFO structure


## -description


Represents the volume tag information. It is used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559417">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a> control code.


## -struct-fields




### -field NumberOfElements

The number of elements matching criteria set forth by the <b>ActionCode</b> member of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551479">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>. 




For information on compatibility with the current device, see the <b>Features0</b> member of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff554979">GET_CHANGER_PARAMETERS</a>.


### -field ElementStatus

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551461">CHANGER_ELEMENT_STATUS</a> structures, one for each element that corresponded with the information passed in with the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff551479">CHANGER_SEND_VOLUME_TAG_INFORMATION</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551461">CHANGER_ELEMENT_STATUS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551479">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559417">IOCTL_CHANGER_QUERY_VOLUME_TAGS</a>
 

 

