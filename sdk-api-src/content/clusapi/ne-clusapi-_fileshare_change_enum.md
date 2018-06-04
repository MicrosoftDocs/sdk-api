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

# _FILESHARE_CHANGE_ENUM enumeration


## -description


Contains the possible change events that are used by the 
    <a href="https://msdn.microsoft.com/f317f162-49b2-43df-a298-e2de707e089a">FILESHARE_CHANGE</a> structure to describe an entry in a 
    file share event notification list.


## -enum-fields




### -field FILESHARE_CHANGE_NONE

This is a place holder value and is not a valid event.


### -field FILESHARE_CHANGE_ADD

A new file share resource has been created and will be included with the other file shares managed by the 
       File Server resource.


### -field FILESHARE_CHANGE_DEL

A file share resource has been deleted and will be removed from the file shares managed by the File Server 
       resource.


### -field FILESHARE_CHANGE_MODIFY

One or more properties of an existing file share resource have been changed.


## -remarks



<b>NNLEN</b> is defined by ClusAPI.h as follows.

<pre class="syntax" xml:space="preserve"><code>#define NNLEN       80                  // Net name length (share name)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/f317f162-49b2-43df-a298-e2de707e089a">FILESHARE_CHANGE</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

