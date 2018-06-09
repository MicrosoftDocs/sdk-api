---
UID: NN:sbe.ISBE2MediaTypeProfile
title: ISBE2MediaTypeProfile
author: windows-sdk-content
description: Implements a media type profile.
old-location: mstv\isbe2mediatypeprofile.htm
old-project: mstv
ms.assetid: b2fb3d08-cbef-4dbf-a60b-8363ccee4fbf
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ISBE2MediaTypeProfile, ISBE2MediaTypeProfile interface [Microsoft TV Technologies], ISBE2MediaTypeProfile interface [Microsoft TV Technologies],described, mstv.isbe2mediatypeprofile, sbe/ISBE2MediaTypeProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2MediaTypeProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2MediaTypeProfile interface


## -description


Implements a media type profile. A <i>media type profile</i> describes a set of streams and their media types, which are used when output pins for a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter are created to specify the media types supported by those pins. The Stream Buffer Source filter implements the <a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a> interface, which you can use to set the media type profile for the filter. 

To obtain a pointer to the <b>ISBE2MediaTypeProfile</b>  interface, call the <a href="https://msdn.microsoft.com/6a4bec40-2c6d-49fb-8977-3c3db2b2b4df">ISBE2Crossbar::GetInitialProfile</a> method for the crossbar, and then use the value returned in the  <i>ppProfile</i> output parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISBE2MediaTypeProfile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISBE2MediaTypeProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISBE2MediaTypeProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f847d4f1-e748-4ed5-bc79-cfff90601379">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83e8b802-d28f-4130-addf-772682ac327f">DeleteStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14c48484-59b0-4e39-8684-9875edfd6556">GetStream</a>
</td>
<td align="left" width="63%">
Gets the media type of a stream that is specified by its index in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f129ed8-3b61-4291-8400-a5f0905c8b49">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the number of streams in the profile.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISBE2MediaTypeProfile)</code>.



