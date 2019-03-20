---
UID: NN:objidl.ILayoutStorage
title: ILayoutStorage (objidl.h)
author: windows-sdk-content
description: The ILayoutStorage interface enables an application to optimize the layout of its compound files for efficient downloading across a slow link.
old-location: stg\ilayoutstorage.htm
tech.root: Stg
ms.assetid: 72201600-4bbb-4346-a13f-927e8463b6ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILayoutStorage, ILayoutStorage interface [Structured Storage], ILayoutStorage interface [Structured Storage],described, _stg_ilayoutstorage, objidl/ILayoutStorage, stg.ilayoutstorage
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILayoutStorage interface


## -description


The 
<b>ILayoutStorage</b> interface enables an application to optimize the layout of its compound files for efficient downloading across a slow link. The goal is to enable a browser or other application to download data in the order in which it will actually be required.

To optimize a compound file, an application  calls <a href="https://msdn.microsoft.com/8b25b32b-f739-406a-96e8-dba687c7f055">CopyTo</a>  to layout a docfile, thus improving performance in most scenarios.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILayoutStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILayoutStorage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/16371d6c-adb9-43c2-80a4-377e94854bbb">BeginMonitor</a>
</td>
<td align="left" width="63%">
Monitors data access to a file.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83b9486b-78b6-473c-9a9a-33f470a4d70f">EndMonitor</a>
</td>
<td align="left" width="63%">
Ends monitoring of data access.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22ae3485-15d9-47e4-988e-fb760e67595b">LayoutScript</a>
</td>
<td align="left" width="63%">
Provides explicit layout instructions.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5db3a26c-595a-4c9b-bb6d-b170eb9864df">ReLayoutDocfile</a>
</td>
<td align="left" width="63%">
Rewrites file using layout information.</p> (Inherited from <b>ILayoutStorage</b>)</td>
</tr>
</table> 

