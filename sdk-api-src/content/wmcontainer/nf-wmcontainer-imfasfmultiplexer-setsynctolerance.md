---
UID: NF:wmcontainer.IMFASFMultiplexer.SetSyncTolerance
title: IMFASFMultiplexer::SetSyncTolerance (wmcontainer.h)
description: Sets the maximum time by which samples from various streams can be out of synchronization.
helpviewer_keywords: ["54aea995-2beb-4c38-a79f-43a539031d95","IMFASFMultiplexer interface [Media Foundation]","SetSyncTolerance method","IMFASFMultiplexer.SetSyncTolerance","IMFASFMultiplexer::SetSyncTolerance","SetSyncTolerance","SetSyncTolerance method [Media Foundation]","SetSyncTolerance method [Media Foundation]","IMFASFMultiplexer interface","mf.imfasfmultiplexer_setsynctolerance","wmcontainer/IMFASFMultiplexer::SetSyncTolerance"]
old-location: mf\imfasfmultiplexer_setsynctolerance.htm
tech.root: mf
ms.assetid: 54aea995-2beb-4c38-a79f-43a539031d95
ms.date: 12/05/2018
ms.keywords: 54aea995-2beb-4c38-a79f-43a539031d95, IMFASFMultiplexer interface [Media Foundation],SetSyncTolerance method, IMFASFMultiplexer.SetSyncTolerance, IMFASFMultiplexer::SetSyncTolerance, SetSyncTolerance, SetSyncTolerance method [Media Foundation], SetSyncTolerance method [Media Foundation],IMFASFMultiplexer interface, mf.imfasfmultiplexer_setsynctolerance, wmcontainer/IMFASFMultiplexer::SetSyncTolerance
req.header: wmcontainer.h
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
 - IMFASFMultiplexer::SetSyncTolerance
 - wmcontainer/IMFASFMultiplexer::SetSyncTolerance
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
 - IMFASFMultiplexer.SetSyncTolerance
---

# IMFASFMultiplexer::SetSyncTolerance


## -description

Sets the maximum time by which samples from various streams can be out of synchronization. The multiplexer will not accept a sample with a time stamp that is out of synchronization with the latest samples from any other stream by an amount that exceeds the synchronization tolerance.

## -parameters

### -param msSyncTolerance [in]

Synchronization tolerance in milliseconds.

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
</table>

## -remarks

The synchronization tolerance is the maximum difference in presentation times at any given point between samples of different streams that the ASF multiplexer can accommodate. That is, if the synchronization tolerance is 3 seconds, no stream can be more than 3 seconds behind any other stream in the time stamps passed to the multiplexer. The multiplexer determines a default synchronization tolerance to use, but this method overrides it (usually to increase it). More tolerance means the potential for greater latency in the multiplexer. If the time stamps are synchronized among the streams, actual latency will be much lower than <i>msSyncTolerance</i>.

## -see-also

<a href="/windows/desktop/medfound/asf-multiplexer">ASF Multiplexer</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>