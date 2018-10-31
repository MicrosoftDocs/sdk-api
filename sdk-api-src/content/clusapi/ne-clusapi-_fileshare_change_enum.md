---
UID: NE:clusapi._FILESHARE_CHANGE_ENUM
title: "_FILESHARE_CHANGE_ENUM"
author: windows-sdk-content
description: Contains the possible change events that are used by the FILESHARE_CHANGE structure to describe an entry in a file share event notification list.
old-location: mscs\fileshare_change_enum.htm
tech.root: mscs
ms.assetid: 36139a95-141c-4f44-9627-9ed6c3fed0c5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PFILESHARE_CHANGE_ENUM, FILESHARE_CHANGE_ADD, FILESHARE_CHANGE_DEL, FILESHARE_CHANGE_ENUM, FILESHARE_CHANGE_ENUM enumeration [Failover Cluster], FILESHARE_CHANGE_MODIFY, FILESHARE_CHANGE_NONE, _FILESHARE_CHANGE_ENUM, clusapi/FILESHARE_CHANGE_ADD, clusapi/FILESHARE_CHANGE_DEL, clusapi/FILESHARE_CHANGE_ENUM, clusapi/FILESHARE_CHANGE_MODIFY, clusapi/FILESHARE_CHANGE_NONE, mscs.fileshare_change_enum"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - ClusAPI.h
api_name:
 - FILESHARE_CHANGE_ENUM
product: Windows
targetos: Windows
req.typenames: FILESHARE_CHANGE_ENUM, *PFILESHARE_CHANGE_ENUM
req.redist: 
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
 

 

