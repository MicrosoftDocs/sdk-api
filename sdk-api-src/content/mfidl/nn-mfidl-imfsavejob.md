---
UID: NN:mfidl.IMFSaveJob
title: IMFSaveJob (mfidl.h)
author: windows-sdk-content
description: Persists media data from a source byte stream to an application-provided byte stream.
old-location: mf\imfsavejob.htm
tech.root: medfound
ms.assetid: 0f38fa60-ed04-40c4-9bb0-b6e196cd9586
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0f38fa60-ed04-40c4-9bb0-b6e196cd9586, IMFSaveJob, IMFSaveJob interface [Media Foundation], IMFSaveJob interface [Media Foundation],described, mf.imfsavejob, mfidl/IMFSaveJob
ms.topic: interface
f1_keywords: ["mfidl/IMFSaveJob"]
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
 - IMFSaveJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSaveJob interface


## -description


Persists media data from a source byte stream to an application-provided byte stream.

The byte stream used for HTTP download implements this interface. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the byte stream, with the service identifier MFNET_SAVEJOB_SERVICE.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSaveJob</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSaveJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSaveJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-beginsave">BeginSave</a>
</td>
<td align="left" width="63%">
Begins saving a Windows Media file to the application's byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-cancelsave">CancelSave</a>
</td>
<td align="left" width="63%">
Cancels the operation started by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-beginsave">BeginSave</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-endsave">EndSave</a>
</td>
<td align="left" width="63%">
Completes the operation started by <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-beginsave">BeginSave</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-getprogress">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of content saved to the provided byte stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

