---
UID: NN:asyncinfo.IAsyncInfo
title: IAsyncInfo (asyncinfo.h)

description: Provides support for asynchronous operations.
old-location: winrt\iasyncinfo.htm
tech.root: WinRT
ms.assetid: 3444e02e-8817-4c23-84d9-1a2d1bf43a52

ms.date: 12/05/2018
ms.keywords: IAsyncInfo, IAsyncInfo interface [Windows Runtime], IAsyncInfo interface [Windows Runtime],described, asyncinfo/IAsyncInfo, winrt.iasyncinfo
ms.topic: interface
f1_keywords: 
 - "asyncinfo/IAsyncInfo"
dev_langs:
 - c++
req.header: asyncinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AsyncInfo.idl
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
 - AsyncInfo.h
api_name:
 - IAsyncInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAsyncInfo interface


## -description


Provides support for asynchronous operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsyncInfo</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IAsyncInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAsyncInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/asyncinfo/nf-asyncinfo-iasyncinfo-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Requests cancellation of the asynchronous operation already in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/asyncinfo/nf-asyncinfo-iasyncinfo-close">Close</a>
</td>
<td align="left" width="63%">
Closes the asynchronous work object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsyncInfo</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/asyncinfo/nf-asyncinfo-iasyncinfo-get_errorcode">ErrorCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the termination status of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/asyncinfo/nf-asyncinfo-iasyncinfo-get_id">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the identifier of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/asyncinfo/nf-asyncinfo-iasyncinfo-get_status">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that indicates the status of the asynchronous operation.

</td>
</tr>
</table> 

