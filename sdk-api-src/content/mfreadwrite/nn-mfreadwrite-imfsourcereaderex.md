---
UID: NN:mfreadwrite.IMFSourceReaderEx
title: IMFSourceReaderEx
author: windows-sdk-content
description: Extends the IMFSourceReader interface.
old-location: mf\imfsourcereaderex.htm
tech.root: medfound
ms.assetid: 59888F9B-C464-4045-AA77-03EE16E2B598
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IMFSourceReaderEx, IMFSourceReaderEx interface [Media Foundation], IMFSourceReaderEx interface [Media Foundation],described, mf.imfsourcereaderex, mfreadwrite/IMFSourceReaderEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfreadwrite.h
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
 - mfreadwrite.h
api_name:
 - IMFSourceReaderEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceReaderEx interface


## -description


Extends the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> interface.

The <a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a> implements this interface in Windows 8. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the Source Reader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReaderEx</b> interface inherits from <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>. <b>IMFSourceReaderEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceReaderEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/493BB3CF-044D-4E83-9FF7-BD2039358501">AddTransformForStream</a>
</td>
<td align="left" width="63%">
Adds a transform, such as an audio or video effect, to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39F2D132-5D2B-4389-AB30-FE2942EC3965">GetTransformForStream</a>
</td>
<td align="left" width="63%">
Gets a pointer to a Media Foundation transform (MFT) for a specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6C0617CA-8F85-4854-9E4B-8F4300FAE8E3">RemoveAllTransformsForStream</a>
</td>
<td align="left" width="63%">
Removes all of the Media Foundation transforms (MFTs) for a specified stream, with the exception of the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/532E8F28-16F4-442E-83D9-C247E8FA7E2A">SetNativeMediaType</a>
</td>
<td align="left" width="63%">
Sets the native media type for a stream on the media source.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

