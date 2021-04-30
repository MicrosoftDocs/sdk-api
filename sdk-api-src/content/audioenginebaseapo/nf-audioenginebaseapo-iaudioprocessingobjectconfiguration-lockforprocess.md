---
UID: NF:audioenginebaseapo.IAudioProcessingObjectConfiguration.LockForProcess
title: IAudioProcessingObjectConfiguration::LockForProcess (audioenginebaseapo.h)
description: The LockForProcess method is used to verify that the APO is locked and ready to process data.
helpviewer_keywords: ["IAudioProcessingObjectConfiguration interface [Audio Devices]","LockForProcess method","IAudioProcessingObjectConfiguration.LockForProcess","IAudioProcessingObjectConfiguration::LockForProcess","LockForProcess","LockForProcess method [Audio Devices]","LockForProcess method [Audio Devices]","IAudioProcessingObjectConfiguration interface","audio.iaudioprocessingobjectconfiguration_lockforprocess","audio_syseffects_r_cdb70452-7705-4acd-9d29-151225d878c8.xml","audioenginebaseapo/IAudioProcessingObjectConfiguration::LockForProcess"]
old-location: audio\iaudioprocessingobjectconfiguration_lockforprocess.htm
tech.root: audio
ms.assetid: e76c9fc5-15ed-497e-a7da-42b8e3642903
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObjectConfiguration interface [Audio Devices],LockForProcess method, IAudioProcessingObjectConfiguration.LockForProcess, IAudioProcessingObjectConfiguration::LockForProcess, LockForProcess, LockForProcess method [Audio Devices], LockForProcess method [Audio Devices],IAudioProcessingObjectConfiguration interface, audio.iaudioprocessingobjectconfiguration_lockforprocess, audio_syseffects_r_cdb70452-7705-4acd-9d29-151225d878c8.xml, audioenginebaseapo/IAudioProcessingObjectConfiguration::LockForProcess
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows Vista and later versions of the Windows operating system.
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
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioProcessingObjectConfiguration::LockForProcess
 - audioenginebaseapo/IAudioProcessingObjectConfiguration::LockForProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioenginebaseapo.idl
 - Audioenginebaseapo.idl.dll
api_name:
 - IAudioProcessingObjectConfiguration.LockForProcess
---

# IAudioProcessingObjectConfiguration::LockForProcess


## -description

The <code>LockForProcess</code> method is used to verify that the APO is locked and ready to process data.

## -parameters

### -param u32NumInputConnections [in]

Number of input connections that are attached to this APO.

### -param ppInputConnections [in]

Connection descriptor for each input connection that is attached to this APO.

### -param u32NumOutputConnections [in]

Number of output connections that are attached to this APO.

### -param ppOutputConnections [in]

Connection descriptor for each output connection that is attached to this APO.

## -returns

The <code>LockForProcess</code> method returns a value of S_OK if the call is completed successfully. At this stage, the APO is locked and is ready to process data.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer was passed to function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_INVALID_CONNECITON_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Invalid connection format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_NUM_CONNECTIONS_INVALID</b></dt>
</dl>
</td>
<td width="60%">
Number of input or output connections not valid on this APO.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APOERR_APO_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
APO is already locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other HRESULTS</b></dt>
</dl>
</td>
<td width="60%">
These failures will be tracked by the audio engine.

</td>
</tr>
</table>

## -remarks

When the <code>LockForProcess</code> method is called, it first performs an internal check to see if the APO has been initialized and is ready to process data. Each APO has different initialization requirements so each APO must define its own Initialize method if needed.

