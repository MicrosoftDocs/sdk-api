---
UID: NN:shobjidl.IStreamAsync
title: IStreamAsync (shobjidl.h)
author: windows-sdk-content
description: Exposes methods to manage input/outpout (I/O) to an asynchronous stream.
old-location: shell\IStreamAsync.htm
tech.root: shell
ms.assetid: 2d436312-3d61-4511-9342-711b2f7d4717
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStreamAsync, IStreamAsync interface [Windows Shell], IStreamAsync interface [Windows Shell],described, _shell_IStreamAsync, shell.IStreamAsync, shobjidl/IStreamAsync
ms.topic: interface
f1_keywords: 
 - "shobjidl/IStreamAsync"
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl.h
api_name:
 - IStreamAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamAsync interface


## -description


Exposes methods to manage input/outpout (I/O) to an asynchronous stream.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamAsync</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. <b>IStreamAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-istreamasync-cancelio">CancelIo</a>
</td>
<td align="left" width="63%">
Marks all pending input/output (I/O) operations as canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-istreamasync-overlappedresult">OverlappedResult</a>
</td>
<td align="left" width="63%">
Retrieves the results of an overlapped operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-istreamasync-readasync">ReadAsync</a>
</td>
<td align="left" width="63%">
Reads information from a stream asynchronously. For example, the Shell implements this interface on file items when transferring them asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-istreamasync-writeasync">WriteAsync</a>
</td>
<td align="left" width="63%">
Writes information to a stream asynchronously. For example, the Shell implements this method on file items when transferring them asynchronously.

</td>
</tr>
</table> 

