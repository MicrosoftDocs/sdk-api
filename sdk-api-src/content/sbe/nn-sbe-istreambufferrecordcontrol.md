---
UID: NN:sbe.IStreamBufferRecordControl
title: IStreamBufferRecordControl (sbe.h)
description: The IStreamBufferRecordControl interface is used to control stream buffer Recording objects.Use the IStreamBufferSink::CreateRecorder method on the Stream Buffer Sink filter to create new Recording objects.
old-location: mstv\istreambufferrecordcontrol.htm
tech.root: mstv
ms.assetid: f196638e-ccbb-4768-96c1-8e1d00361831
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecordControl, IStreamBufferRecordControl interface [Microsoft TV Technologies], IStreamBufferRecordControl interface [Microsoft TV Technologies],described, IStreamBufferRecordControlInterface, mstv.istreambufferrecordcontrol, sbe/IStreamBufferRecordControl
f1_keywords:
- sbe/IStreamBufferRecordControl
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
- COM
api_location:
- Sbe.h
api_name:
- IStreamBufferRecordControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferRecordControl interface


## -description



The <b>IStreamBufferRecordControl</b> interface is used to control stream buffer <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/recording-object">Recording</a> objects.

Use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-createrecorder">IStreamBufferSink::CreateRecorder</a> method on the Stream Buffer Sink filter to create new Recording objects. After making a recording, stop the <b>Recording</b> object and release it before releasing the Stream Buffer Sink filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferRecordControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferRecordControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferRecordControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-getrecordingstatus">GetRecordingStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the <b>Recording</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-start">Start</a>
</td>
<td align="left" width="63%">
Starts a recording at a specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-stop">Stop</a>
</td>
<td align="left" width="63%">
Ends a recording at a specified time.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecordControl)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/creating-stream-buffer-recordings">Creating Stream Buffer Recordings</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

