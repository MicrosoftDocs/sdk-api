---
UID: NN:strmif.IAMOpenProgress
title: IAMOpenProgress
author: windows-sdk-content
description: The IAMOpenProgress interface reports the progress of a file-open operation and enables the application to cancel the operation.Filters that open files over a network can expose this interface.
old-location: dshow\iamopenprogress.htm
tech.root: DirectShow
ms.assetid: 31021c83-ee83-49c3-a089-31184756fb0d
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMOpenProgress, IAMOpenProgress interface [DirectShow], IAMOpenProgress interface [DirectShow],described, IAMOpenProgressInterface, dshow.iamopenprogress, strmif/IAMOpenProgress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMOpenProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMOpenProgress interface


## -description



The <code>IAMOpenProgress</code> interface reports the progress of a file-open operation and enables the application to cancel the operation.

Filters that open files over a network can expose this interface. An application can use it to query the progress of the download, or to cancel the download. If the network is not responsive, a method such as <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a> might block for an indefinite period. To prevent your application from blocking, create a worker thread that uses <code>IAMOpenProgress</code> to monitor the progress. The worker thread can cancel the operation if a predefined timeout occurs, or in response to a command from the user.

The <a href="https://msdn.microsoft.com/405fd6ea-aa17-4d11-8f07-067468cb090b">File Source (URL)</a> filter supports this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMOpenProgress</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMOpenProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMOpenProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c20b57c-c491-4465-9626-13335191b5bb">AbortOperation</a>
</td>
<td align="left" width="63%">
Cancels the file-open operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8471271d-36cc-4660-8a4e-4c234ba6b406">QueryProgress</a>
</td>
<td align="left" width="63%">
Retrieves the progress of the file-open operation.

</td>
</tr>
</table> 

