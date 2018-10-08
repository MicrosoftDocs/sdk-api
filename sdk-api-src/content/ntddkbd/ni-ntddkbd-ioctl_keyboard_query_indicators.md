---
UID: NI:ntddkbd.IOCTL_KEYBOARD_QUERY_INDICATORS
title: IOCTL_KEYBOARD_QUERY_INDICATORS
author: windows-sdk-content
description: The IOCTL_KEYBOARD_QUERY_INDICATORS request returns information about the keyboard indicators.
old-location: hid\ioctl_keyboard_query_indicators2.htm
tech.root: hid
ms.assetid: ca031026-a077-4270-addd-a0a8c22f46b6
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IOCTL_KEYBOARD_QUERY_INDICATORS, IOCTL_KEYBOARD_QUERY_INDICATORS control, IOCTL_KEYBOARD_QUERY_INDICATORS control code [Human Input Devices], hid.ioctl_keyboard_query_indicators2, i8042ref_d34933a9-dfd8-464b-9653-7b344b5007e3.xml, ntddkbd/IOCTL_KEYBOARD_QUERY_INDICATORS
ms.prod: windows
ms.technology: windows-sdk
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
 - IOCTL_KEYBOARD_QUERY_INDICATORS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_KEYBOARD_QUERY_INDICATORS IOCTL


## -description


The IOCTL_KEYBOARD_QUERY_INDICATORS request returns information about the keyboard indicators.


## -ioctlparameters




### -input-buffer

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is set to a value greater than or equal to the size, in bytes, of a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -input-buffer-length

The size of a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -output-buffer

<b>AssociatedIrp.SystemBuffer</b> points to a client-allocated buffer that I8042prt uses to output a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -output-buffer-length

The size of  a <a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a> structure.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the request is successful, the <b>Information</b> member is set to the size, in bytes, of a KEYBOARD_INDICATOR_PARAMETERS structure. Otherwise, <b>Information</b> is set to zero.

The <b>Status</b> member is set to one the following values:




#### -STATUS_BUFFER_TOO_SMALL

<b>Parameters.DeviceIoControl.OutputBufferLength</b> is less than the size, in bytes, of a KEYBOARD_INDICATOR_PARAMETERS structure.


#### -STATUS_SUCCESS

The request completed successfully.


## -see-also




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/68c9d24a-c1c9-4ef6-904d-6aeb68cea32a">KEYBOARD_INDICATOR_PARAMETERS</a>
 

 

