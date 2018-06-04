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

# _VDS_PORT_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties 
   of a port on a controller object.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> assigned to the port.


### -field pwszFriendlyName

The name of the port; a zero-terminated, human-readable string.


### -field pwszIdentification

The port identifier or address, typically a world wide name (WWN); a zero-terminated, human-readable 
      string.

For Fibre Channel networks, this member should be the WWN for the port, formatted as a hexadecimal string (16 characters long), most significant byte first. For example, a WWN address of 01:23:45:67:89:AB:CD:EF should be represented as "0123456789ABCDEF".


### -field status

The status of the port enumerated by 
      <a href="https://msdn.microsoft.com/6e363020-caf4-4028-abd5-7f311edb2e69">VDS_PORT_STATUS</a>.


## -remarks



The 
    <a href="https://msdn.microsoft.com/01972923-2a43-4a80-80f8-8dab4207bbc4">IVdsController::GetPortProperties</a> 
    method returns this structure to report the property details of a port on a controller object.




## -see-also




<a href="https://msdn.microsoft.com/01972923-2a43-4a80-80f8-8dab4207bbc4">IVdsController::GetPortProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/6e363020-caf4-4028-abd5-7f311edb2e69">VDS_PORT_STATUS</a>
 

 

