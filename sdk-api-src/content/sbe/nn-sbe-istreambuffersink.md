---
UID: NN:sbe.IStreamBufferSink
title: IStreamBufferSink (sbe.h)
author: windows-sdk-content
description: The IStreamBufferSink interface is exposed by the Stream Buffer Sink filter. Use this interface to lock the filter before capture and to create new recordings.
old-location: mstv\istreambuffersink.htm
tech.root: mstv
ms.assetid: 4ae5a9e9-da51-4034-9a2c-22b57374deac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStreamBufferSink, IStreamBufferSink interface [Microsoft TV Technologies], IStreamBufferSink interface [Microsoft TV Technologies],described, IStreamBufferSinkInterface, mstv.istreambuffersink, sbe/IStreamBufferSink
ms.topic: interface
f1_keywords: 
 - "sbe/IStreamBufferSink"
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
 - IStreamBufferSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferSink interface


## -description



The <b>IStreamBufferSink</b> interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter. Use this interface to lock the filter before capture and to create new recordings.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-createrecorder">CreateRecorder</a>
</td>
<td align="left" width="63%">
Creates a <b>Recording</b> object for permanent file storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-isprofilelocked">IsProfileLocked</a>
</td>
<td align="left" width="63%">
Indicates whether the profile has been locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-lockprofile">LockProfile</a>
</td>
<td align="left" width="63%">
Locks a graph profile, preventing input streams from changing, and optionally specifies the buffer file's name and location.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferSink)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/using-the-stream-buffer-engine">Using the Stream Buffer Engine</a>
 

 

