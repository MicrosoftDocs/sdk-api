---
UID: NN:mfidl.IMFNetCrossOriginSupport
title: IMFNetCrossOriginSupport
author: windows-sdk-content
description: Implemented by clients that want to enforce a cross origin policy for HTML5 media downloads.
old-location: mf\imfnetcrossoriginsupport.htm
tech.root: MedFound
ms.assetid: 239E5731-4425-46D4-AFEC-F3E59258B1DF
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFNetCrossOriginSupport, IMFNetCrossOriginSupport interface [Media Foundation], IMFNetCrossOriginSupport interface [Media Foundation],described, mf.imfnetcrossoriginsupport, mfidl/IMFNetCrossOriginSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IMFNetCrossOriginSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFNetCrossOriginSupport interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Implemented by clients that want to enforce a cross origin policy for HTML5 media downloads. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetCrossOriginSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFNetCrossOriginSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetCrossOriginSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="mf.imfnetcrossoriginsupport_getcrossoriginpolicy">GetCrossOriginPolicy</a>
</td>
<td align="left" width="63%">
Returns the client's current cross-origin policy to apply to the download session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="mf.imfnetcrossoriginsupport_getsourceorigin">GetSourceOrigin</a>
</td>
<td align="left" width="63%">
Returns the W3C origin of the HTML5 media element.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="mf.imfnetcrossoriginsupport_issameorigin">IsSameOrigin</a>
</td>
<td align="left" width="63%">
Returns true when the specified URL has the same origin as the HTML5 media element.

</td>
</tr>
</table> 


## -remarks



The Media Foundation network code uses these client callbacks to implement and enforce cross origin downloads.



