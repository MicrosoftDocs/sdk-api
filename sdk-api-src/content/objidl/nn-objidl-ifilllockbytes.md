---
UID: NN:objidl.IFillLockBytes
title: IFillLockBytes (objidl.h)
description: The IFillLockBytes interface enables downloading code to write data asynchronously to a structured storage byte array.
helpviewer_keywords: ["IFillLockBytes","IFillLockBytes interface [Structured Storage]","IFillLockBytes interface [Structured Storage]","described","_stg_ifilllockbytes","objidl/IFillLockBytes","stg.ifilllockbytes"]
old-location: stg\ifilllockbytes.htm
tech.root: Stg
ms.assetid: 033b3db4-3ff0-4cb4-916f-2490e92f5e6a
ms.date: 12/05/2018
ms.keywords: IFillLockBytes, IFillLockBytes interface [Structured Storage], IFillLockBytes interface [Structured Storage],described, _stg_ifilllockbytes, objidl/IFillLockBytes, stg.ifilllockbytes
f1_keywords:
- objidl/IFillLockBytes
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IFillLockBytes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFillLockBytes interface


## -description


The 
<b>IFillLockBytes</b> interface enables downloading code to write data asynchronously to a structured storage byte array. When the downloading code has new data available, it calls 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillappend">IFillLockBytes::FillAppend</a> or <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillat">IFillLockBytes::FillAt</a> to write the data to the byte array. An application attempting to access this data, through calls to the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface, can do so even as the downloader continues to make calls to 
<b>IFillLockBytes</b>. If the application attempts to access data that has not already been downloaded through a call to 
<b>IFillLockBytes</b>, then 
<b>ILockBytes</b> returns a new error, E_PENDING.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFillLockBytes</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFillLockBytes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFillLockBytes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillappend">FillAppend</a>
</td>
<td align="left" width="63%">
Writes a new block of bytes to end of byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-fillat">FillAt</a>
</td>
<td align="left" width="63%">
Writes a new block of bytes to specified location in byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-setfillsize">SetFillSize</a>
</td>
<td align="left" width="63%">
Sets expected size of byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ifilllockbytes-terminate">Terminate</a>
</td>
<td align="left" width="63%">
Notifies byte array wrapper of successful or unsuccessful termination of download.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms774966(v=vs.85)">BINDINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iprogressnotify">IProgressNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>
 

 

