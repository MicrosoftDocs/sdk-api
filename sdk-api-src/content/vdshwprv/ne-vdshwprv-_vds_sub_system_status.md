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

# _VDS_SUB_SYSTEM_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   set of object status values for a subsystem.


## -enum-fields




### -field VDS_SSS_UNKNOWN

This value is reserved.


### -field VDS_SSS_ONLINE

The subsystem is working properly.


### -field VDS_SSS_NOT_READY

The subsystem is initializing and not yet ready to work.


### -field VDS_SSS_OFFLINE


      The subsystem is unavailable. This value indicates either that the subsystem is disconnected or that it has 
      failed so severely that it appears to be disconnected.


### -field VDS_SSS_FAILED


      The subsystem has failed. This value indicates that the subsystem is not merely 
      disconnected but rather that it has failed.


### -field VDS_SSS_PARTIALLY_MANAGED

The subsystem is operating in a degraded state. This means that one or more of the subsystem's subcomponents, such as  disk drives or controllers, are in a failed state.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks




    The <a href="https://msdn.microsoft.com/07104aac-acdc-447c-9a30-ff3318f6df09">IVdsSubSystem::SetStatus</a> method passes a <b>VDS_SUB_SYSTEM_STATUS</b> 
    value as an argument to set the status of a subsystem, and the 
    <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> structure includes a <b>VDS_SUB_SYSTEM_STATUS</b> value 
    as a member to indicate the current status.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_SUB_SYSTEM_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_SUB_SYSTEM_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/07104aac-acdc-447c-9a30-ff3318f6df09">IVdsSubSystem::SetStatus</a>



<a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a>
 

 

