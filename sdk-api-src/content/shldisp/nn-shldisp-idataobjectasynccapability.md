---
UID: NN:shldisp.IDataObjectAsyncCapability
title: IDataObjectAsyncCapability (shldisp.h)
author: windows-sdk-content
description: Enables interfaces that are usually synchronous to function asynchronously.
old-location: shell\IDataObjectAsyncCapability.htm
tech.root: shell
ms.assetid: 2E23A137-0C5B-4ce9-8100-758C7E17753B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDataObjectAsyncCapability, IDataObjectAsyncCapability interface [Windows Shell], IDataObjectAsyncCapability interface [Windows Shell],described, shell.IDataObjectAsyncCapability, shldisp/IDataObjectAsyncCapability
ms.topic: interface
f1_keywords: ["shldisp/IDataObjectAsyncCapability"]
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDataObjectAsyncCapability
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataObjectAsyncCapability interface


## -description


Enables interfaces that are usually synchronous to function asynchronously.
        
            
<div class="alert"><b>Note</b>  This interface is the current, renamed version of <a href="https://docs.microsoft.com/previous-versions/bb776309(v=vs.85)">IAsyncOperation</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataObjectAsyncCapability</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataObjectAsyncCapability</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataObjectAsyncCapability</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-endoperation">EndOperation</a>
</td>
<td align="left" width="63%">
Notifies the data object that the asynchronous data extraction has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode">GetAsyncMode</a>
</td>
<td align="left" width="63%">
Called by a drop target to determine whether the data object supports asynchronous data extraction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-inoperation">InOperation</a>
</td>
<td align="left" width="63%">
Called by the drop source to determine whether the target is extracting data asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode">SetAsyncMode</a>
</td>
<td align="left" width="63%">
Called by a drop source to specify whether the data object supports asynchronous data extraction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-startoperation">StartOperation</a>
</td>
<td align="left" width="63%">
Called by a drop target to indicate that asynchronous data extraction is starting.

</td>
</tr>
</table> 


## -remarks



<b>IDataObjectAsyncCapability</b> is an optional interface that is implemented by a data object. It allows the drop target to negotiate with the drop source to extract data from the data object asynchronously.

This interface is primarily exported by the data objects used with drag-and-drop and Clipboard operations. Typically, such operations are synchronous. However, if data rendering will be time-consuming, <b>IDataObjectAsyncCapability</b> can be used to allow data extraction to take place on a background thread. See the <i>Dragging and Dropping Shell Objects Asynchronously</i> section of <a href="https://docs.microsoft.com/windows/desktop/shell/datascenarios">Handling Shell Data Transfer Scenarios</a> for a detailed discussion of how to use this interface.

Drop sources and targets use this interface when they wish to have a lengthy data extraction process handled by a background thread.



