---
UID: NN:strmif.IMediaPropertyBag
title: IMediaPropertyBag
author: windows-sdk-content
description: The IMediaPropertyBag interface is exposed by the Media Property Bag object.
old-location: dshow\imediapropertybag.htm
old-project: DirectShow
ms.assetid: 6f134160-b0aa-44fd-b1b9-938f11349eac
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMediaPropertyBag, IMediaPropertyBag interface [DirectShow], IMediaPropertyBag interface [DirectShow],described, IMediaPropertyBagInterface, dshow.imediapropertybag, strmif/IMediaPropertyBag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaPropertyBag
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaPropertyBag interface


## -description



The <code>IMediaPropertyBag</code> interface is exposed by the <a href="https://msdn.microsoft.com/06678d57-c00b-4575-84e7-3d09f65f19ba">Media Property Bag</a> object. The Media Property Bag is a specialized version of the standard COM property bag, designed for setting and retrieving INFO and DISP chunks in Audio-Video Interleaved (AVI) files.

An INFO chunk contains meta-information about a file, such as author and copyright information. A DISP chunk contains data in Clipboard format. For more information, refer to the resource interchange file format (RIFF) specification.

The media property bag stores the chunks as name/value pairs, as follows:

<ul>
<li>INFO chunks: The name is a string with the form INFO/XXXX, where XXXX is the four-character code that defines the type of meta-information—for example, ICOP for copyright information and IART for author name. The value is any string.</li>
<li>DISP chunks: The name is a string with the form DISP/0000000000, where 0000000000 is the 10-character decimal equivalent of a standard Clipboard format—for example, 0000000008 for CF_DIB. The value is an array of bytes that contains the display data.</li>
</ul>
Use this interface with the <a href="https://msdn.microsoft.com/33e4b76b-841a-4dc5-b117-e08a6f4dcbe7">IPersistMediaPropertyBag</a> interface to retrieve INFO and DISP chunks from an AVI file.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaPropertyBag</b> interface inherits from <b>IPropertyBag</b>. <b>IMediaPropertyBag</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaPropertyBag</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88cd9016-ef6f-467a-9e84-10b2ac578211">EnumProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property/value pair.

</td>
</tr>
</table> 

