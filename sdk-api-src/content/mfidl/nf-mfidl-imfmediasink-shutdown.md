---
UID: NF:mfidl.IMFMediaSink.Shutdown
title: IMFMediaSink::Shutdown (mfidl.h)
description: Shuts down the media sink and releases the resources it is using.
helpviewer_keywords: ["IMFMediaSink interface [Media Foundation]","Shutdown method","IMFMediaSink.Shutdown","IMFMediaSink::Shutdown","Shutdown","Shutdown method [Media Foundation]","Shutdown method [Media Foundation]","IMFMediaSink interface","acda4e37-2dd0-4322-90fc-8f48d6842054","mf.imfmediasink_shutdown","mfidl/IMFMediaSink::Shutdown"]
old-location: mf\imfmediasink_shutdown.htm
tech.root: mf
ms.assetid: acda4e37-2dd0-4322-90fc-8f48d6842054
ms.date: 12/05/2018
ms.keywords: IMFMediaSink interface [Media Foundation],Shutdown method, IMFMediaSink.Shutdown, IMFMediaSink::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFMediaSink interface, acda4e37-2dd0-4322-90fc-8f48d6842054, mf.imfmediasink_shutdown, mfidl/IMFMediaSink::Shutdown
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFMediaSink::Shutdown
 - mfidl/IMFMediaSink::Shutdown
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
 - IMFMediaSink.Shutdown
---

# IMFMediaSink::Shutdown


## -description

Shuts down the media sink and releases the resources it is using.



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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink was shut down.

</td>
</tr>
</table>

## -remarks

If the application creates the media sink, it is responsible for calling <b>Shutdown</b> to avoid memory or resource leaks. In most applications, however, the application creates an activation object for the media sink, and the Media Session uses that object to create the media sink. In that case, the Media Session — not the application — shuts down the media sink. (For more information, see <a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>.)

After this method returns, all methods on the media sink return MF_E_SHUTDOWN,  except for <b>IUnknown</b> methods and <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> methods. The sink will not raise any events after this method is called.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>
