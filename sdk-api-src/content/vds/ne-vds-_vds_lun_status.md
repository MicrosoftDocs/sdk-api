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

# _VDS_LUN_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a LUN.


## -enum-fields




### -field VDS_LS_UNKNOWN

This value is reserved.


### -field VDS_LS_ONLINE

The LUN is available.


### -field VDS_LS_NOT_READY

The LUN is busy.


### -field VDS_LS_OFFLINE

The LUN is unavailable.


### -field VDS_LS_FAILED

The LUN has failed.


## -remarks



The  <a href="https://msdn.microsoft.com/a293f129-5238-405a-ba56-bf53ac4ab1d8">IVdsLun::SetStatus</a>
      method passes a <b>VDS_LUN_STATUS</b> value as an argument to set the status of a LUN, and the <a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a> structure includes a <b>VDS_LUN_STATUS</b> value as a member to indicate the current status.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a293f129-5238-405a-ba56-bf53ac4ab1d8">
        IVdsLun::SetStatus</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">
        VDS_LUN_PROP</a>
 

 

