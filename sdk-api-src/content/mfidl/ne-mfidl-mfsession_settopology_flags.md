---
UID: NE:mfidl.MFSESSION_SETTOPOLOGY_FLAGS
title: MFSESSION_SETTOPOLOGY_FLAGS
author: windows-driver-content
description: Defines the behavior of the IMFMediaSession::SetTopology method.
old-location: mf\mfsession_settopology_flags.htm
old-project: medfound
ms.assetid: 2993bdf9-cf28-4e20-9f38-f51fb0f6429e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 2993bdf9-cf28-4e20-9f38-f51fb0f6429e, MFSESSION_SETTOPOLOGY_CLEAR_CURRENT, MFSESSION_SETTOPOLOGY_FLAGS, MFSESSION_SETTOPOLOGY_FLAGS enumeration [Media Foundation], MFSESSION_SETTOPOLOGY_IMMEDIATE, MFSESSION_SETTOPOLOGY_NORESOLUTION, mf.mfsession_settopology_flags, mfidl/MFSESSION_SETTOPOLOGY_CLEAR_CURRENT, mfidl/MFSESSION_SETTOPOLOGY_FLAGS, mfidl/MFSESSION_SETTOPOLOGY_IMMEDIATE, mfidl/MFSESSION_SETTOPOLOGY_NORESOLUTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSESSION_SETTOPOLOGY_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfidl.h
api_name:
-	MFSESSION_SETTOPOLOGY_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

