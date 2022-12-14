---
UID: NE:mfapi.__unnamed_enum_1
title: MF_TOPOSTATUS (mfapi.h)
description: Specifies the status of a topology during playback.
helpviewer_keywords: ["7cf2a4f2-c115-4dee-ab91-6a3fab33365f","MF_TOPOSTATUS","MF_TOPOSTATUS enumeration [Media Foundation]","MF_TOPOSTATUS_DYNAMIC_CHANGED","MF_TOPOSTATUS_ENDED","MF_TOPOSTATUS_INVALID","MF_TOPOSTATUS_READY","MF_TOPOSTATUS_SINK_SWITCHED","MF_TOPOSTATUS_STARTED_SOURCE","mf.mf_topostatus","mfapi/MF_TOPOSTATUS","mfapi/MF_TOPOSTATUS_DYNAMIC_CHANGED","mfapi/MF_TOPOSTATUS_ENDED","mfapi/MF_TOPOSTATUS_INVALID","mfapi/MF_TOPOSTATUS_READY","mfapi/MF_TOPOSTATUS_SINK_SWITCHED","mfapi/MF_TOPOSTATUS_STARTED_SOURCE"]
old-location: mf\mf_topostatus.htm
tech.root: mf
ms.assetid: 7cf2a4f2-c115-4dee-ab91-6a3fab33365f
ms.date: 12/05/2018
ms.keywords: 7cf2a4f2-c115-4dee-ab91-6a3fab33365f, MF_TOPOSTATUS, MF_TOPOSTATUS enumeration [Media Foundation], MF_TOPOSTATUS_DYNAMIC_CHANGED, MF_TOPOSTATUS_ENDED, MF_TOPOSTATUS_INVALID, MF_TOPOSTATUS_READY, MF_TOPOSTATUS_SINK_SWITCHED, MF_TOPOSTATUS_STARTED_SOURCE, mf.mf_topostatus, mfapi/MF_TOPOSTATUS, mfapi/MF_TOPOSTATUS_DYNAMIC_CHANGED, mfapi/MF_TOPOSTATUS_ENDED, mfapi/MF_TOPOSTATUS_INVALID, mfapi/MF_TOPOSTATUS_READY, mfapi/MF_TOPOSTATUS_SINK_SWITCHED, mfapi/MF_TOPOSTATUS_STARTED_SOURCE
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
targetos: Windows
req.typenames: MF_TOPOSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_TOPOSTATUS
 - mfapi/MF_TOPOSTATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MF_TOPOSTATUS
---

# MF_TOPOSTATUS enumeration


## -description

Specifies the status of a topology during playback.

## -enum-fields

### -field MF_TOPOSTATUS_INVALID:0

This value is not used.

### -field MF_TOPOSTATUS_READY:100

The topology is ready to start. After this status flag is received, you can use the Media Session's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> method to query the topology for services, such as rate control.

### -field MF_TOPOSTATUS_STARTED_SOURCE:200

The Media Session has started to read data from the media sources in the topology.

### -field MF_TOPOSTATUS_DYNAMIC_CHANGED:210

The Media Session modified the topology, because the format of a stream changed.

### -field MF_TOPOSTATUS_SINK_SWITCHED:300

The media sinks have switched from the previous topology to this topology. This status value is not sent for the first topology that is played. For the first topology, the <a href="/windows/desktop/medfound/mesessionstarted">MESessionStarted</a> event indicates that the media sinks have started receiving data.

### -field MF_TOPOSTATUS_ENDED:400

Playback of this topology is complete. The Media Session might still use the topology internally. The Media Session does not completely release the topology until it sends the next <b>MF_TOPOSTATUS_STARTED_SOURCE</b> status event or the <a href="/windows/desktop/medfound/mesessionended">MESessionEnded</a> event.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mesessiontopologystatus">MESessionTopologyStatus</a> event. The MESessionTopologyStatus event always has an <a href="/windows/desktop/medfound/mf-event-topology-status-attribute">MF_EVENT_TOPOLOGY_STATUS</a> attribute whose value is a member of this enumeration.
      

For a single topology, the Media Session sends these status flags in numerical order, starting with <b>MF_TOPOSTATUS_READY</b>. However, there is no guarantee about the ordering of the events across two different topologies. For example, you might get <b>MF_TOPOSTATUS_READY</b> for a topology before you get <b>MF_TOPOSTATUS_ENDED</b> for the previous topology.

## -see-also

<a href="/windows/desktop/medfound/mesessiontopologystatus">MESessionTopologyStatus</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
