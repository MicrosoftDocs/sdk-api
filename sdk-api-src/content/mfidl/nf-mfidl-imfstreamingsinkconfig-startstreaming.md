---
UID: NF:mfidl.IMFStreamingSinkConfig.StartStreaming
title: IMFStreamingSinkConfig::StartStreaming (mfidl.h)
description: Called by the streaming media client before the Media Session starts streaming to specify the byte offset or the time offset.
helpviewer_keywords: ["FALSE","IMFStreamingSinkConfig interface [Media Foundation]","StartStreaming method","IMFStreamingSinkConfig.StartStreaming","IMFStreamingSinkConfig::StartStreaming","StartStreaming","StartStreaming method [Media Foundation]","StartStreaming method [Media Foundation]","IMFStreamingSinkConfig interface","TRUE","mf.imfstreamingsinkconfig_startstreaming","mfidl/IMFStreamingSinkConfig::StartStreaming"]
old-location: mf\imfstreamingsinkconfig_startstreaming.htm
tech.root: mf
ms.assetid: 22a75b19-9949-48fe-8844-511b11fbf20b
ms.date: 12/05/2018
ms.keywords: FALSE, IMFStreamingSinkConfig interface [Media Foundation],StartStreaming method, IMFStreamingSinkConfig.StartStreaming, IMFStreamingSinkConfig::StartStreaming, StartStreaming, StartStreaming method [Media Foundation], StartStreaming method [Media Foundation],IMFStreamingSinkConfig interface, TRUE, mf.imfstreamingsinkconfig_startstreaming, mfidl/IMFStreamingSinkConfig::StartStreaming
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFStreamingSinkConfig::StartStreaming
 - mfidl/IMFStreamingSinkConfig::StartStreaming
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFStreamingSinkConfig.StartStreaming
---

# IMFStreamingSinkConfig::StartStreaming


## -description

Called by the streaming media client before the Media Session starts streaming to specify the byte offset or the time offset.

## -parameters

### -param fSeekOffsetIsByteOffset [in]

    A Boolean value that specifies whether <i>qwSeekOffset</i> gives a byte offset of a time offset.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>qwSeekOffset</i> parameter specifies a byte offset.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>qwSeekOffset</i> parameter specifies the time position in 100-nanosecond units.

</td>
</tr>
</table>

### -param qwSeekOffset [in]

A byte offset or a time offset, depending on the value passed in <i>fSeekOffsetIsByteOffset</i>.  Time offsets are specified in
    100-nanosecond units.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamingsinkconfig">IMFStreamingSinkConfig</a>