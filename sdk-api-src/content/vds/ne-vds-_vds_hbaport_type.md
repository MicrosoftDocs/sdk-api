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

# _VDS_HBAPORT_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   set of valid types for an HBA port. These types correspond to the HBA_PORTTYPE values in the HBA API.


## -enum-fields




### -field VDS_HPT_UNKNOWN

The port type is unknown.
     

HBA_PORTTYPE_UNKNOWN


### -field VDS_HPT_OTHER

The port type is another (undefined) type.
     

HBA_PORTTYPE_OTHER


### -field VDS_HPT_NOTPRESENT

The port type is not present.
     

HBA_PORTTYPE_NOTPRESENT


### -field VDS_HPT_NPORT

The port type is a fabric.
     

HBA_PORTTYPE_NPORT


### -field VDS_HPT_NLPORT

The port type is a public loop.
     

HBA_PORTTYPE_NLPORT


### -field VDS_HPT_FLPORT

The port type is a fabric on a loop.
     

HBA_PORTTYPE_FLPORT


### -field VDS_HPT_FPORT

The port type is a fabric port.
     

HBA_PORTTYPE_FPORT


### -field VDS_HPT_EPORT

The port type is a fabric expansion port.
     




### -field VDS_HPT_GPORT

The port type is a generic fabric port.
     




### -field VDS_HPT_LPORT

The port type is a private loop.
     

HBA_PORTTYPE_LPORT


### -field VDS_HPT_PTP

The port type is point-to-point.
     

HBA_PORTTYPE_PTP


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HBAPORT_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HBAPORT_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

