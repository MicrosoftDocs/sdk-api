---
UID: NF:mfidl.IMFStreamSink.PlaceMarker
title: IMFStreamSink::PlaceMarker
author: windows-sdk-content
description: Places a marker in the stream.
old-location: mf\imfstreamsink_placemarker.htm
tech.root: medfound
ms.assetid: bfa4fb12-59b2-4599-b8ff-dc38750a5a79
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFStreamSink interface [Media Foundation],PlaceMarker method, IMFStreamSink.PlaceMarker, IMFStreamSink::PlaceMarker, PlaceMarker, PlaceMarker method [Media Foundation], PlaceMarker method [Media Foundation],IMFStreamSink interface, bfa4fb12-59b2-4599-b8ff-dc38750a5a79, mf.imfstreamsink_placemarker, mfidl/IMFStreamSink::PlaceMarker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFStreamSink.PlaceMarker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFStreamSink::PlaceMarker


## -description



Places a marker in the stream. 




## -parameters




### -param eMarkerType [in]

Specifies the marker type, as a member of the <a href="https://msdn.microsoft.com/d1c5f8ee-a451-44af-bf43-7623cea2be37">MFSTREAMSINK_MARKER_TYPE</a> enumeration.
          


### -param pvarMarkerValue [in]

Optional pointer to a <b>PROPVARIANT</b> that contains additional information related to the marker. The meaning of this value depends on the marker type. This parameter can be <b>NULL</b>.
          


### -param pvarContextValue [in]

Optional pointer to a <b>PROPVARIANT</b> that is attached to the <a href="https://msdn.microsoft.com/40f68352-86e5-4864-9ca0-f30998857fef">MEStreamSinkMarker</a> event. Call <a href="https://msdn.microsoft.com/05e57b40-2565-4312-866e-50f0c7d62c4a">IMFMediaEvent::GetValue</a> to get this value from the event. The caller can use this information for any purpose. This parameter can be <b>NULL</b>.
          


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">Shutdown</a> method has been called.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_STREAMSINK_REMOVED</b></b></dt>
</dl>
</td>
<td width="60%">
This stream was removed from the media sink and is no longer valid.
              

</td>
</tr>
</table>
 




## -remarks



This method causes the stream sink to send an <a href="https://msdn.microsoft.com/40f68352-86e5-4864-9ca0-f30998857fef">MEStreamSinkMarker</a> event after the stream sink consumes all of the samples that were delivered up to this point (before the call to <b>PlaceMarker</b>).




## -see-also




<a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

