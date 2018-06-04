---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagDVTARGETDEVICE structure


## -description


Specifies information about the target device for which data is being composed. <b>DVTARGETDEVICE</b> contains enough information about a Windows target device so a handle to a device context (<b>HDC</b>) can be created using the <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a> function. 




## -struct-fields




### -field tdSize

The size, in bytes, of the <b>DVTARGETDEVICE</b> structure. The initial size is included so the structure can be copied more easily.


### -field tdDriverNameOffset

The offset, in bytes, from the beginning of the structure to the device driver name, which is stored as a NULL-terminated string in the <b>tdData</b> buffer.


### -field tdDeviceNameOffset

The offset, in bytes, from the beginning of the structure to the device name, which is stored as a NULL-terminated string in the <b>tdData</b> buffer. This value can be zero to indicate no device name.


### -field tdPortNameOffset

The offset, in bytes, from the beginning of the structure to the port name, which is stored as a NULL-terminated string in the <b>tdData</b> buffer. This value can be zero to indicate no port name.


### -field tdExtDevmodeOffset

The offset, in bytes, from the beginning of the structure to the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure retrieved by calling <a href="https://msdn.microsoft.com/e89a2f6f-2bac-4369-b526-f8e15028698b">DocumentProperties</a>.


### -field tdData

An array of bytes containing data for the target device. It is not necessary to include empty strings in <b>tdData</b> (for names where the offset value is zero).



## -remarks



Some OLE 1 client applications incorrectly construct target devices by allocating too few bytes in the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure for the <b>DVTARGETDEVICE</b>. They typically only supply the number of bytes in the <b>dmSize</b> member of <b>DEVMODE</b>. The number of bytes to be allocated should be the sum of <b>dmSize</b> + <b>dmDriverExtra</b>. When a call is made to the <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a> function with an incorrect target device, the printer driver tries to access the additional bytes and unpredictable results can occur. To help protect against a crash and make the additional bytes available, OLE pads the size of OLE 2 target devices created from OLE 1 target devices.




## -see-also




<a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>



<a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a>



<a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>



<a href="https://msdn.microsoft.com/8fed879c-5f97-4450-8259-da9643dd828c">OleConvertOLESTREAMToIStorage</a>
 

 

