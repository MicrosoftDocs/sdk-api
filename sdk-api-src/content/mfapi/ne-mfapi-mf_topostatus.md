---
UID: NE:mfapi.MF_TOPOSTATUS
title: MF_TOPOSTATUS
author: windows-sdk-content
description: Specifies the status of a topology during playback.
old-location: mf\mf_topostatus.htm
tech.root: medfound
ms.assetid: 7cf2a4f2-c115-4dee-ab91-6a3fab33365f
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 7cf2a4f2-c115-4dee-ab91-6a3fab33365f, MF_TOPOSTATUS, MF_TOPOSTATUS enumeration [Media Foundation], MF_TOPOSTATUS_DYNAMIC_CHANGED, MF_TOPOSTATUS_ENDED, MF_TOPOSTATUS_INVALID, MF_TOPOSTATUS_READY, MF_TOPOSTATUS_SINK_SWITCHED, MF_TOPOSTATUS_STARTED_SOURCE, mf.mf_topostatus, mfapi/MF_TOPOSTATUS, mfapi/MF_TOPOSTATUS_DYNAMIC_CHANGED, mfapi/MF_TOPOSTATUS_ENDED, mfapi/MF_TOPOSTATUS_INVALID, mfapi/MF_TOPOSTATUS_READY, mfapi/MF_TOPOSTATUS_SINK_SWITCHED, mfapi/MF_TOPOSTATUS_STARTED_SOURCE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MF_TOPOSTATUS
product: Windows
targetos: Windows
req.typenames: MF_TOPOSTATUS
req.redist: 
---

# MF_TOPOSTATUS enumeration


## -description


Specifies the status of a topology during playback.
        


## -enum-fields




### -field MF_TOPOSTATUS_INVALID

This value is not used.
          


### -field MF_TOPOSTATUS_READY

The topology is ready to start. After this status flag is received, you can use the Media Session's <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> method to query the topology for services, such as rate control.
          


### -field MF_TOPOSTATUS_STARTED_SOURCE

The Media Session has started to read data from the media sources in the topology.
          


### -field MF_TOPOSTATUS_DYNAMIC_CHANGED

The Media Session modified the topology, because the format of a stream changed.


### -field MF_TOPOSTATUS_SINK_SWITCHED

The media sinks have switched from the previous topology to this topology. This status value is not sent for the first topology that is played. For the first topology, the <a href="https://msdn.microsoft.com/28ed32f0-9b23-4da1-9587-15f490da7bf9">MESessionStarted</a> event indicates that the media sinks have started receiving data.
          


### -field MF_TOPOSTATUS_ENDED

Playback of this topology is complete. The Media Session might still use the topology internally. The Media Session does not completely release the topology until it sends the next <b>MF_TOPOSTATUS_STARTED_SOURCE</b> status event or the <a href="https://msdn.microsoft.com/e593e51f-c239-49e9-bba8-c6d8238eff24">MESessionEnded</a> event.
          


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/b45fd598-ab1e-4b12-8d82-c88c96d1f770">MESessionTopologyStatus</a> event. The MESessionTopologyStatus event always has an <a href="https://msdn.microsoft.com/f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1">MF_EVENT_TOPOLOGY_STATUS</a> attribute whose value is a member of this enumeration.
      

For a single topology, the Media Session sends these status flags in numerical order, starting with <b>MF_TOPOSTATUS_READY</b>. However, there is no guarantee about the ordering of the events across two different topologies. For example, you might get <b>MF_TOPOSTATUS_READY</b> for a topology before you get <b>MF_TOPOSTATUS_ENDED</b> for the previous topology.
      




## -see-also




<a href="https://msdn.microsoft.com/b45fd598-ab1e-4b12-8d82-c88c96d1f770">MESessionTopologyStatus</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

