---
UID: NC:resapi.POFFLINE_ROUTINE
title: POFFLINE_ROUTINE
author: windows-sdk-content
description: Marks a resource as unavailable for use after cleanup processing is complete.
old-location: mscs\offline.htm
tech.root: mscs
ms.assetid: 1d67a4f5-66f8-4818-8b63-d0f50452f889
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Offline, Offline callback, Offline callback function [Failover Cluster], POFFLINE_ROUTINE, POFFLINE_ROUTINE callback function [Failover Cluster], _wolf_offline, mscs.offline, resapi/Offline, resapi/POFFLINE_ROUTINE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - Offline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# POFFLINE_ROUTINE callback function


## -description


Marks a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as unavailable for use after cleanup 
    processing is complete. The <b>POFFLINE_ROUTINE</b> type defines a pointer to 
    this function.


## -parameters




### -param Resource [in]

Resource identifier for the resource to be taken offline.


## -returns



If the operation was not successful for other reasons, 
       <i>Offline</i> should return one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



If <i>Offline</i> returns an error code other than 
     <b>ERROR_IO_PENDING</b>, the 
     <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> logs an event and calls 
     <a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>.

For effective implementation strategies of the <i>Offline</i> 
     entry-point function, see <a href="https://msdn.microsoft.com/d6459783-cb94-4fbc-b76d-da811db379ce">Implementing Offline</a>.


#### Examples

See <a href="https://msdn.microsoft.com/library/Aa372246(v=VS.85).aspx">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c">NetShareDel</a>



<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry Point Functions</a>
 

 

