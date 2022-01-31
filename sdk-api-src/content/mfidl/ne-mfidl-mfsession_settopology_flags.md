---
UID: NE:mfidl.MFSESSION_SETTOPOLOGY_FLAGS
title: MFSESSION_SETTOPOLOGY_FLAGS (mfidl.h)
description: Defines the behavior of the IMFMediaSession::SetTopology method.
helpviewer_keywords: ["2993bdf9-cf28-4e20-9f38-f51fb0f6429e","MFSESSION_SETTOPOLOGY_CLEAR_CURRENT","MFSESSION_SETTOPOLOGY_FLAGS","MFSESSION_SETTOPOLOGY_FLAGS enumeration [Media Foundation]","MFSESSION_SETTOPOLOGY_IMMEDIATE","MFSESSION_SETTOPOLOGY_NORESOLUTION","mf.mfsession_settopology_flags","mfidl/MFSESSION_SETTOPOLOGY_CLEAR_CURRENT","mfidl/MFSESSION_SETTOPOLOGY_FLAGS","mfidl/MFSESSION_SETTOPOLOGY_IMMEDIATE","mfidl/MFSESSION_SETTOPOLOGY_NORESOLUTION"]
old-location: mf\mfsession_settopology_flags.htm
tech.root: mf
ms.assetid: 2993bdf9-cf28-4e20-9f38-f51fb0f6429e
ms.date: 12/05/2018
ms.keywords: 2993bdf9-cf28-4e20-9f38-f51fb0f6429e, MFSESSION_SETTOPOLOGY_CLEAR_CURRENT, MFSESSION_SETTOPOLOGY_FLAGS, MFSESSION_SETTOPOLOGY_FLAGS enumeration [Media Foundation], MFSESSION_SETTOPOLOGY_IMMEDIATE, MFSESSION_SETTOPOLOGY_NORESOLUTION, mf.mfsession_settopology_flags, mfidl/MFSESSION_SETTOPOLOGY_CLEAR_CURRENT, mfidl/MFSESSION_SETTOPOLOGY_FLAGS, mfidl/MFSESSION_SETTOPOLOGY_IMMEDIATE, mfidl/MFSESSION_SETTOPOLOGY_NORESOLUTION
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFSESSION_SETTOPOLOGY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFSESSION_SETTOPOLOGY_FLAGS
 - mfidl/MFSESSION_SETTOPOLOGY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFSESSION_SETTOPOLOGY_FLAGS
---

# MFSESSION_SETTOPOLOGY_FLAGS enumeration


## -description

Defines the behavior of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">IMFMediaSession::SetTopology</a> method.

## -enum-fields

### -field MFSESSION_SETTOPOLOGY_IMMEDIATE:0x1

Stop the current presentation, clear all pending presentations, and immediately queue the new topology (specified by the <i>pTopology</i> parameter).

If the <i>pTopology</i>  parameter is <b>NULL</b>, this flag has no effect.

### -field MFSESSION_SETTOPOLOGY_NORESOLUTION:0x2

The topology does not need to be resolved. Use this flag if you are setting a full topology.

### -field MFSESSION_SETTOPOLOGY_CLEAR_CURRENT:0x4

<div class="alert"><b>Note</b>  Requires Windows 7.</div>
<div> </div>
Clear the current topology, as follows:

<ul>
<li>If <i>pTopology</i> is not <b>NULL</b>, the topology is cleared only if  <i>pTopology</i> matches the current topology (that is, only if <i>pTopology</i> points to the current topology). </li>
<li>If the <i>pTopology</i> parameter is <b>NULL</b>, the current topology is cleared, regardless of which topology is current.</li>
</ul>
Pending topologies are not removed from the playback queue. If there is a pending topology on the queue, that topology will be loaded after the current topology is cleared. Otherwise, playback simply stops.

To remove all of the pending topologies from the queue, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies">IMFMediaSession::ClearTopologies</a>.

## -remarks

These flags are optional, and are not mutually exclusive. If no flags are set, the Media Session resolves the topology and then adds it to the queue of pending presentations.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
