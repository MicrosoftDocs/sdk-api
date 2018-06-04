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

# _VDS_CONTROLLER_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a controller.


## -enum-fields




### -field VDS_CS_UNKNOWN

The status of the controller cannot be determined.


### -field VDS_CS_ONLINE

The controller is physically present and in use. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value associated with this controller status can be any value except <b>VDS_H_FAILED</b>.


### -field VDS_CS_NOT_READY

The controller is busy. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value can be any value except <b>VDS_H_FAILED</b>.


### -field VDS_CS_OFFLINE

The controller is physically present but not available for use. For example, the controller has been set to the inactive state. When this controller status is set, a <b>VDS_NF_CONTROLLER_REMOVED</b> notification is sent.  The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value can be any value.


### -field VDS_CS_FAILED

The controller has failed. The <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> value should be <b>VDS_H_FAILED</b> or <b>VDS_H_FAILING</b>.


### -field VDS_CS_REMOVED

The controller has been physically unplugged from the subsystem. When this status is set, a <b>VDS_NF_CONTROLLER_DEPART</b> notification is sent.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



The <a href="https://msdn.microsoft.com/f9bae451-ef47-46ad-a11e-b7b36a031a8a">
        IVdsController::SetStatus</a>
      method passes a <b>VDS_CONTROLLER_STATUS</b> value as an argument to set the status of a controller, and  the <a href="https://msdn.microsoft.com/b9da3920-9bae-4198-ba0d-a0755aee15e4">VDS_CONTROLLER_PROP</a> structure includes a <b>VDS_CONTROLLER_STATUS</b> value as a member to indicate the current status.

If your application encounters a <b>VDS_CONTROLLER_STATUS</b> value that it does not recognize, it should display the controller status as unknown. It should not attempt to map the unrecognized controller status to another controller status.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_CONTROLLER_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_CONTROLLER_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f9bae451-ef47-46ad-a11e-b7b36a031a8a">
        IVdsController::SetStatus</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/b9da3920-9bae-4198-ba0d-a0755aee15e4">
        VDS_CONTROLLER_PROP</a>
 

 

