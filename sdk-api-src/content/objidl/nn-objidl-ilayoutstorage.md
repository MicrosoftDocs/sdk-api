---
UID: NN:objidl.ILayoutStorage
title: ILayoutStorage (objidl.h)
author: windows-sdk-content
description: The ILayoutStorage interface enables an application to optimize the layout of its compound files for efficient downloading across a slow link.
old-location: stg\ilayoutstorage.htm
tech.root: Stg
ms.assetid: 72201600-4bbb-4346-a13f-927e8463b6ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILayoutStorage, ILayoutStorage interface [Structured Storage], ILayoutStorage interface [Structured Storage],described, _stg_ilayoutstorage, objidl/ILayoutStorage, stg.ilayoutstorage
ms.topic: interface
f1_keywords: 
 - "objidl/ILayoutStorage"
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
 - ILayoutStorage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILayoutStorage interface


## -description


The 
<b>ILayoutStorage</b> interface enables an application to optimize the layout of its compound files for efficient downloading across a slow link. The goal is to enable a browser or other application to download data in the order in which it will actually be required.

To optimize a compound file, an application  calls <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-copyto">CopyTo</a>  to layout a docfile, thus improving performance in most scenarios.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILayoutStorage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILayoutStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILayoutStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-beginmonitor">BeginMonitor</a>
</td>
<td align="left" width="63%">
Monitors data access to a file.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-endmonitor">EndMonitor</a>
</td>
<td align="left" width="63%">
Ends monitoring of data access.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-layoutscript">LayoutScript</a>
</td>
<td align="left" width="63%">
Provides explicit layout instructions.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-relayoutdocfile">ReLayoutDocfile</a>
</td>
<td align="left" width="63%">
Rewrites file using layout information.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
</table> 

