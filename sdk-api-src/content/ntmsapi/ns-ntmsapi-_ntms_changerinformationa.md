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

# _NTMS_CHANGERINFORMATIONA structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_CHANGERINFORMATION</b> structure defines properties specific to a robotic changer object.


## -struct-fields




### -field Number

Number of the changer within the library.


### -field ChangerType

Identifier of the changer type of this changer.


### -field szSerialNumber

Serial number for the changer represented as a string. Devices that do not support serial numbers report <b>NULL</b> for this member.


### -field szRevision

Revision for the changer, represented as a string.


### -field szDeviceName

Name of the device used to access the changer.


### -field ScsiPort

SCSI host adapter to which the changer is connected.


### -field ScsiBus

SCSI bus to which the changer is connected.


### -field ScsiTarget

SCSI target ID for the changer.


### -field ScsiLun

SCSI logical unit ID for the changer.


### -field Library

Unique identifier of the library that contains the changer.


## -remarks



The 
<b>NTMS_CHANGERINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

