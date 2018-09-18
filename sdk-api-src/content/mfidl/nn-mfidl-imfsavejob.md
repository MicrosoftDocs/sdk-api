---
UID: NN:mfidl.IMFSaveJob
title: IMFSaveJob
author: windows-sdk-content
description: Persists media data from a source byte stream to an application-provided byte stream.
old-location: mf\imfsavejob.htm
tech.root: medfound
ms.assetid: 0f38fa60-ed04-40c4-9bb0-b6e196cd9586
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 0f38fa60-ed04-40c4-9bb0-b6e196cd9586, IMFSaveJob, IMFSaveJob interface [Media Foundation], IMFSaveJob interface [Media Foundation],described, mf.imfsavejob, mfidl/IMFSaveJob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IMFSaveJob interface


## -description


Persists media data from a source byte stream to an application-provided byte stream.

The byte stream used for HTTP download implements this interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> on the byte stream, with the service identifier MFNET_SAVEJOB_SERVICE.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSaveJob</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSaveJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ff137b76-2a05-4e58-8d4f-d12cdd89656b">BeginSave</a>
</td>
<td align="left" width="63%">
Begins saving a Windows Media file to the application's byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce3ec53a-eeca-430f-a939-3d941b9b2570">CancelSave</a>
</td>
<td align="left" width="63%">
Cancels the operation started by <a href="https://msdn.microsoft.com/ff137b76-2a05-4e58-8d4f-d12cdd89656b">BeginSave</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d63d7b5-4454-4301-b467-eea82bace6ff">EndSave</a>
</td>
<td align="left" width="63%">
Completes the operation started by <a href="https://msdn.microsoft.com/ff137b76-2a05-4e58-8d4f-d12cdd89656b">BeginSave</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8782333c-796c-4401-9575-c78e95887015">GetProgress</a>
</td>
<td align="left" width="63%">
Retrieves the percentage of content saved to the provided byte stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

