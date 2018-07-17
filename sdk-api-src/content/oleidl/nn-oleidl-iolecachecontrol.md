---
UID: NN:oleidl.IOleCacheControl
title: IOleCacheControl
author: windows-sdk-content
description: Provides proper maintenance of caches. It maintains the caches by connecting the running object's IDataObject implementation to the cache, allowing the cache to receive notifications from the running object.
old-location: com\iolecachecontrol.htm
old-project: com
ms.assetid: 64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IOleCacheControl, IOleCacheControl interface [COM], IOleCacheControl interface [COM],described, _ole_iolecachecontrol, com.iolecachecontrol, oleidl/IOleCacheControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleCacheControl
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: ADAM
---

# IOleCacheControl interface


## -description


Provides proper maintenance of caches. It maintains the caches by connecting the running object's <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> implementation to the cache, allowing the cache to receive notifications from the running object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleCacheControl</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOleCacheControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleCacheControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d155c3f-115c-41fe-985f-ed60a565341f">OnRun</a>
</td>
<td align="left" width="63%">
Notifies the cache that the data source object has entered the running state so that the cache object can establish advise sinks as needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95e62e9d-39bd-4bf8-ba25-c6a9c7fc515b">OnStop</a>
</td>
<td align="left" width="63%">
Notifies the cache that it should terminate any existing advise sinks.

</td>
</tr>
</table> 

