---
UID: NN:d2d1_1.ID2D1GdiMetafileSink
title: ID2D1GdiMetafileSink
author: windows-sdk-content
description: A developer implemented interface that allows a metafile to be replayed.
old-location: direct2d\id2d1gdimetafilesink.htm
tech.root: direct2d
ms.assetid: 1E9866C3-2A07-48C2-A4C5-F9AE3C7B2272
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID2D1GdiMetafileSink, ID2D1GdiMetafileSink interface [Direct2D], ID2D1GdiMetafileSink interface [Direct2D],described, d2d1_1/ID2D1GdiMetafileSink, direct2d.id2d1gdimetafilesink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GdiMetafileSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GdiMetafileSink interface


## -description


A developer implemented interface that allows a metafile to be replayed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GdiMetafileSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1GdiMetafileSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GdiMetafileSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2133C62-A689-4FE6-8E9D-39E161EEFCE1">ProcessRecord</a>
</td>
<td align="left" width="63%">
 This method is called once for each record stored in a metafile.

</td>
</tr>
</table> 

