---
UID: NN:shldisp.IDataObjectAsyncCapability
title: IDataObjectAsyncCapability
author: windows-sdk-content
description: Enables interfaces that are usually synchronous to function asynchronously.
old-location: shell\IDataObjectAsyncCapability.htm
old-project: shell
ms.assetid: 2E23A137-0C5B-4ce9-8100-758C7E17753B
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDataObjectAsyncCapability, IDataObjectAsyncCapability interface [Windows Shell], IDataObjectAsyncCapability interface [Windows Shell],described, shell.IDataObjectAsyncCapability, shldisp/IDataObjectAsyncCapability
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IDataObjectAsyncCapability
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IDataObjectAsyncCapability interface


## -description


Enables interfaces that are usually synchronous to function asynchronously.
        
            
<div class="alert"><b>Note</b>  This interface is the current, renamed version of <a href="https://msdn.microsoft.com/a20e6057-c46a-4dbf-88b0-5dc954dc0362">IAsyncOperation</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataObjectAsyncCapability</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDataObjectAsyncCapability</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/CF9D2A95-12AF-4538-882D-B391F2E087ED">EndOperation</a>
</td>
<td align="left" width="63%">
Notifies the data object that the asynchronous data extraction has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0B7A4299-4D19-4c5a-99A5-9568F4D58061">GetAsyncMode</a>
</td>
<td align="left" width="63%">
Called by a drop target to determine whether the data object supports asynchronous data extraction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/858EB8C4-88AB-40a3-B4FC-CCD19235CE55">InOperation</a>
</td>
<td align="left" width="63%">
Called by the drop source to determine whether the target is extracting data asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97DCCA78-F25E-47de-8292-F0C6ED9DFD35">SetAsyncMode</a>
</td>
<td align="left" width="63%">
Called by a drop source to specify whether the data object supports asynchronous data extraction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84C1E709-ADFD-4c00-B767-C0DB4C30578A">StartOperation</a>
</td>
<td align="left" width="63%">
Called by a drop target to indicate that asynchronous data extraction is starting.

</td>
</tr>
</table> 


## -remarks



<b>IDataObjectAsyncCapability</b> is an optional interface that is implemented by a data object. It allows the drop target to negotiate with the drop source to extract data from the data object asynchronously.

This interface is primarily exported by the data objects used with drag-and-drop and Clipboard operations. Typically, such operations are synchronous. However, if data rendering will be time-consuming, <b>IDataObjectAsyncCapability</b> can be used to allow data extraction to take place on a background thread. See the <i>Dragging and Dropping Shell Objects Asynchronously</i> section of <a href="https://msdn.microsoft.com/7fce555c-a93d-4414-9119-7ae9acdd4d89">Handling Shell Data Transfer Scenarios</a> for a detailed discussion of how to use this interface.

Drop sources and targets use this interface when they wish to have a lengthy data extraction process handled by a background thread.



