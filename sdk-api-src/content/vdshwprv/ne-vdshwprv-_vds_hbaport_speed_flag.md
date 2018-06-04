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

# _VDS_HBAPORT_SPEED_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for determining the speeds supported by an HBA port. 
    These values are used in the <b>ulPortSpeed</b> member of the 
    <a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a> structure.
   


## -enum-fields




### -field VDS_HSF_UNKNOWN


      The HBA port speed is unknown. The transceiver is incapable of reporting.
      

HBA_PORTSPEED_UNKNOWN


### -field VDS_HSF_1GBIT


      The HBA port supports a transfer rate of 1 gigabit per second.
      

HBA_PORTSPEED_1GBIT


### -field VDS_HSF_2GBIT


      The HBA port supports a transfer rate of 2 gigabits per second.
      

HBA_PORTSPEED_2GBIT


### -field VDS_HSF_10GBIT


      The HBA port supports a transfer rate of 10 gigabits per second.
      

HBA_PORTSPEED_10GBIT


### -field VDS_HSF_4GBIT


      The HBA port supports a transfer rate of 4 gigabits per second.
      

HBA_PORTSPEED_4GBIT


### -field VDS_HSF_NOT_NEGOTIATED


      The HBA port speed has not been established.
      

HBA_PORTSPEED_NOT_NEGOTIATED


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HBAPORT_SPEED_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HBAPORT_SPEED_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c">VDS_HBAPORT_PROP</a>
 

 

