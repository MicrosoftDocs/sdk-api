---
UID: NN:dwrite_3.IDWriteRemoteFontFileLoader
title: IDWriteRemoteFontFileLoader
author: windows-sdk-content
description: Represents a font file loader that can access remote (i.e., downloadable) fonts.
old-location: directwrite\idwriteremotefontfileloader.htm
tech.root: DirectWrite
ms.assetid: 16CFF7ED-642A-48D8-8C72-3EC68B702E50
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteRemoteFontFileLoader, IDWriteRemoteFontFileLoader interface [Direct Write], IDWriteRemoteFontFileLoader interface [Direct Write],described, directwrite.idwriteremotefontfileloader, dwrite_3/IDWriteRemoteFontFileLoader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteRemoteFontFileLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRemoteFontFileLoader interface


## -description


Represents a font file loader that can access remote (i.e., downloadable) fonts. The <a href="https://msdn.microsoft.com/7C8D581E-489D-48BE-8B3F-278E1C246BBA">IDWriteFactory5::CreateHttpFontFileLoader</a> method returns an instance of this interface,
        which the client can use to load remote fonts without having to implement a custom loader. 
        A client can also create its own custom implementation, however. 
        In either case, the client is responsible for registering and unregistering the loader using IDWriteFactory::<a href="https://msdn.microsoft.com/f5b28c3d-c3ad-4435-92c8-07841e8d160a">RegisterFontFileLoader</a> 
        and IDWriteFactory::<a href="https://msdn.microsoft.com/f048671e-dfb6-449d-9bcd-e5df8408c01a">UnregisterFontFileLoader</a>.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteRemoteFontFileLoader</b> interface inherits from <a href="https://msdn.microsoft.com/855e281e-3855-4c11-af87-68f8e0dadbf8">IDWriteFontFileLoader</a>. <b>IDWriteRemoteFontFileLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteRemoteFontFileLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8695514-532F-4CAC-9A50-049C81812F15">CreateFontFileReferenceFromUrl</a>
</td>
<td align="left" width="63%">
Creates a font file reference from a URL if the loader supports this capability.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/434B7349-0FD3-492F-8973-600A0A0DFA7B">CreateRemoteStreamFromKey</a>
</td>
<td align="left" width="63%">
Creates a remote font file stream object that encapsulates an open file resource and can be used to download remote file data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/997D8F04-8667-4D90-B097-CD48F979BE02">GetLocalityFromKey</a>
</td>
<td align="left" width="63%">
Gets the locality of the file resource identified by the unique key.

</td>
</tr>
</table> 


## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_known_remote_fonts_on_the_Web">Creating a custom font set using known, remote fonts on the Web</a>



<a href="https://msdn.microsoft.com/855e281e-3855-4c11-af87-68f8e0dadbf8">IDWriteFontFileLoader</a>
 

 

