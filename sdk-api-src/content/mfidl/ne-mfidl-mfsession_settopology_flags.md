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

# MFSESSION_SETTOPOLOGY_FLAGS enumeration


## -description



Defines the behavior of the <a href="https://msdn.microsoft.com/ea5313f0-b0fd-4945-97a2-b3f17937294f">IMFMediaSession::SetTopology</a> method.




## -enum-fields




### -field MFSESSION_SETTOPOLOGY_IMMEDIATE

Stop the current presentation, clear all pending presentations, and immediately queue the new topology (specified by the <i>pTopology</i> parameter).

If the <i>pTopology</i>  parameter is <b>NULL</b>, this flag has no effect.


### -field MFSESSION_SETTOPOLOGY_NORESOLUTION


            The topology does not need to be resolved. Use this flag if you are setting a full topology.
          


### -field MFSESSION_SETTOPOLOGY_CLEAR_CURRENT

<div class="alert"><b>Note</b>  Requires Windows 7.</div>
<div> </div>
Clear the current topology, as follows:

<ul>
<li>If <i>pTopology</i> is not <b>NULL</b>, the topology is cleared only if  <i>pTopology</i> matches the current topology (that is, only if <i>pTopology</i> points to the current topology). </li>
<li>If the <i>pTopology</i> parameter is <b>NULL</b>, the current topology is cleared, regardless of which topology is current.</li>
</ul>
Pending topologies are not removed from the playback queue. If there is a pending topology on the queue, that topology will be loaded after the current topology is cleared. Otherwise, playback simply stops.

To remove all of the pending topologies from the queue, call <a href="https://msdn.microsoft.com/fcb7e5f1-1095-4766-afed-43ad2279abb4">IMFMediaSession::ClearTopologies</a>.


## -remarks




        These flags are optional, and are not mutually exclusive. If no flags are set, the Media Session resolves the topology and then adds it to the queue of pending presentations.
      




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

