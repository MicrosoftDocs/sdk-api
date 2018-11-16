---
UID: NN:mfidl.IMFMediaSourceEx
title: IMFMediaSourceEx
author: windows-sdk-content
description: Extends the IMFMediaSource interface to provide additional capabilities for a media source.
old-location: mf\imfmediasourceex.htm
tech.root: medfound
ms.assetid: C72C79D5-FD65-4F27-A8C8-B94BF5A9E829
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMFMediaSourceEx, IMFMediaSourceEx interface [Media Foundation], IMFMediaSourceEx interface [Media Foundation],described, mf.imfmediasourceex, mfidl/IMFMediaSourceEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFMediaSourceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSourceEx interface


## -description


Extends the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface to provide additional capabilities for a media source.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the media source. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceEx</b> interface inherits from <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a>. <b>IMFMediaSourceEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourceEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A58A2537-1ABD-4EC5-AC84-A5FFA7127CEB">GetSourceAttributes</a>
</td>
<td align="left" width="63%">
Gets an attribute store for the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/360B64E6-4936-4E40-A0EB-7E9EBAF1203E">GetStreamAttributes</a>
</td>
<td align="left" width="63%">
Gets an attribute store for a stream on the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9E956E68-9950-4AA1-BF43-C1DCB02393F7">SetD3DManager</a>
</td>
<td align="left" width="63%">
Sets a pointer to the DXGI Device Manager on the media source.

</td>
</tr>
</table> 


## -remarks



Implementations of this interface can return <b>E_NOTIMPL</b> for any methods that are not required by the media source.




## -see-also




<a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

