---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
title: IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION (ntddkbd.h)
author: windows-sdk-content
description: The IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION request returns information about the mapping between scan codes and keyboard indicators.
old-location: hid\ioctl_keyboard_query_indicator_translation2.htm
tech.root: hid
ms.assetid: b8d139e1-9465-41bd-b5e3-bc8f79f85d96
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION, IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION control, IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION control code [Human Input Devices], hid.ioctl_keyboard_query_indicator_translation2, i8042ref_e1b419fa-c16e-4fe4-9534-5ae074cbb238.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
ms.topic: ioctl
req.header: ntddkbd.h
req.include-header: Ntddkbd.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ntddkbd.h
api_name:
 - IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION IOCTL


## -description


The IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION request returns information about the mapping between scan codes and keyboard indicators.


## -ioctlparameters




### -input-buffer

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a device-specific <a href="https://msdn.microsoft.com/7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a">KEYBOARD_INDICATOR_TRANSLATION</a> structure. This structure includes a variable-sized array of INDICATOR_LIST members that is device-specific.


### -input-buffer-length

 The size of a <a href="https://msdn.microsoft.com/7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a">KEYBOARD_INDICATOR_TRANSLATION</a> structure.


### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that I8042prt uses to output a <a href="https://msdn.microsoft.com/7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a">KEYBOARD_INDICATOR_TRANSLATION</a> structure. This structure includes a variable-sized array of INDICATOR_LIST members that is device-specific.


### -output-buffer-length

 The size of a <a href="https://msdn.microsoft.com/7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a">KEYBOARD_INDICATOR_TRANSLATION</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of the device-specific KEYBOARD_INDICATOR_TRANSLATION structure. Otherwise, <b>Information</b> is set to zero.

The <b>Status</b> member is set to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of the device-specific KEYBOARD_INDICATOR_TRANSLATION structure.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a">KEYBOARD_INDICATOR_TRANSLATION</a>
 

 

