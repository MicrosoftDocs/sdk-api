---
UID: NF:mfidl.IMFMediaSession.ClearTopologies
title: IMFMediaSession::ClearTopologies (mfidl.h)
description: Clears all of the presentations that are queued for playback in the Media Session.
helpviewer_keywords: ["ClearTopologies","ClearTopologies method [Media Foundation]","ClearTopologies method [Media Foundation]","IMFMediaSession interface","IMFMediaSession interface [Media Foundation]","ClearTopologies method","IMFMediaSession.ClearTopologies","IMFMediaSession::ClearTopologies","fcb7e5f1-1095-4766-afed-43ad2279abb4","mf.imfmediasession_cleartopologies","mfidl/IMFMediaSession::ClearTopologies"]
old-location: mf\imfmediasession_cleartopologies.htm
tech.root: mf
ms.assetid: fcb7e5f1-1095-4766-afed-43ad2279abb4
ms.date: 12/05/2018
ms.keywords: ClearTopologies, ClearTopologies method [Media Foundation], ClearTopologies method [Media Foundation],IMFMediaSession interface, IMFMediaSession interface [Media Foundation],ClearTopologies method, IMFMediaSession.ClearTopologies, IMFMediaSession::ClearTopologies, fcb7e5f1-1095-4766-afed-43ad2279abb4, mf.imfmediasession_cleartopologies, mfidl/IMFMediaSession::ClearTopologies
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSession::ClearTopologies
 - mfidl/IMFMediaSession::ClearTopologies
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSession.ClearTopologies
---

# IMFMediaSession::ClearTopologies


## -description

Clears all of the presentations that are queued for playback in the Media Session.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed in the Media Session's current state.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The Media Session has been shut down.
              

</td>
</tr>
</table>

## -remarks

This method is asynchronous. When the operation completes, the Media Session sends an <a href="/windows/desktop/medfound/mesessiontopologiescleared">MESessionTopologiesCleared</a> event.

This method does not clear the current topology; it only removes topologies that are placed in the queue, waiting for playback. To remove the current topology, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">IMFMediaSession::SetTopology</a> with the <b>MFSESSION_SETTOPOLOGY_CLEAR_CURRENT</b> flag.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>
