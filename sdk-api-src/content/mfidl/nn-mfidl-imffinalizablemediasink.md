---
UID: NN:mfidl.IMFFinalizableMediaSink
title: IMFFinalizableMediaSink (mfidl.h)
author: windows-sdk-content
description: Optionally supported by media sinks to perform required tasks before shutdown.
old-location: mf\imffinalizablemediasink.htm
tech.root: medfound
ms.assetid: e60c2773-f2fc-469e-a698-036390cbed16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFFinalizableMediaSink, IMFFinalizableMediaSink interface [Media Foundation], IMFFinalizableMediaSink interface [Media Foundation],described, e60c2773-f2fc-469e-a698-036390cbed16, mf.imffinalizablemediasink, mfidl/IMFFinalizableMediaSink
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFFinalizableMediaSink"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFFinalizableMediaSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFFinalizableMediaSink interface


## -description


Optionally supported by media sinks to perform required tasks before shutdown. This interface is typically exposed by archive sinks—that is, media sinks that write to a file. It is used to perform tasks such as flushing data to disk or updating a file header.

To get a pointer to this interface, call <b>QueryInterface</b> on the media sink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFFinalizableMediaSink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>. <b>IMFFinalizableMediaSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFFinalizableMediaSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize">BeginFinalize</a>
</td>
<td align="left" width="63%">
Notifies the media sink to complete its final tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-endfinalize">EndFinalize</a>
</td>
<td align="left" width="63%">
Called when the asynchronous callback given to <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize">BeginFinalize</a> is invoked.

</td>
</tr>
</table> 


## -remarks



If a media sink exposes this interface, the Media Session will call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize">BeginFinalize</a> on the sink before the session closes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

