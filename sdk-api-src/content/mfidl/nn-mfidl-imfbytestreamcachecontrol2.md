---
UID: NN:mfidl.IMFByteStreamCacheControl2
title: IMFByteStreamCacheControl2
author: windows-sdk-content
description: Controls how a network byte stream transfers data to a local cache.
old-location: mf\imfbytestreamcachecontrol2.htm
old-project: medfound
ms.assetid: A901F679-B6F2-4DB7-8EFC-EA61249B64FB
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFByteStreamCacheControl2, IMFByteStreamCacheControl2 interface [Media Foundation], IMFByteStreamCacheControl2 interface [Media Foundation],described, mf.imfbytestreamcachecontrol2, mfidl/IMFByteStreamCacheControl2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamCacheControl2
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamCacheControl2 interface


## -description


Controls how a network byte stream transfers data to a local cache. This interface extends the <a href="https://msdn.microsoft.com/e12a532a-4624-4e06-8e19-6e9daec550ac">IMFByteStreamCacheControl</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFByteStreamCacheControl2</b> interface inherits from <a href="https://msdn.microsoft.com/e12a532a-4624-4e06-8e19-6e9daec550ac">IMFByteStreamCacheControl</a>. <b>IMFByteStreamCacheControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFByteStreamCacheControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FC91FCB5-CD22-494F-85B7-38571C38A44E">GetByteRanges</a>
</td>
<td align="left" width="63%">
Gets the ranges of bytes that are currently stored in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FC08E5E8-A7E0-461C-B70C-B1273FCDD1A0">IsBackgroundTransferActive</a>
</td>
<td align="left" width="63%">
Queries whether background transfer is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1DDC3D76-E28B-4B8C-B2CD-FE77E840D949">SetCacheLimit</a>
</td>
<td align="left" width="63%">
Limits the cache size.

</td>
</tr>
</table> 


## -remarks



Byte streams object in Microsoft Media Foundation can optionally implement this interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the byte stream object. 




## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>



<a href="https://msdn.microsoft.com/e12a532a-4624-4e06-8e19-6e9daec550ac">IMFByteStreamCacheControl</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

