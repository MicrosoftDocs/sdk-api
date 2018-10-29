---
UID: NN:strmif.ISeekingPassThru
title: ISeekingPassThru
author: windows-sdk-content
description: The ISeekingPassThru interface creates a helper object that implements seeking for one-input filters.
old-location: dshow\iseekingpassthru.htm
tech.root: DirectShow
ms.assetid: a22f2723-b44e-4c7e-8508-db5c6af5b1d6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ISeekingPassThru, ISeekingPassThru interface [DirectShow], ISeekingPassThru interface [DirectShow],described, ISeekingPassThruInterface, dshow.iseekingpassthru, strmif/ISeekingPassThru
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ISeekingPassThru
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISeekingPassThru interface


## -description



The <code>ISeekingPassThru</code> interface creates a helper object that implements seeking for one-input filters. Filters can use this interface to implement the <a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking</a> and <a href="https://msdn.microsoft.com/325dd9a4-80ca-43e3-9ff8-473df1b833e9">IMediaPosition</a> interfaces. For more information, see <a href="https://msdn.microsoft.com/14180d6e-7925-4e1a-8b16-cae9d7113468">CPosPassThru</a>.

Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISeekingPassThru</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISeekingPassThru</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISeekingPassThru</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb32c20c-bbae-403a-885b-f07c6dcf46f4">Init</a>
</td>
<td align="left" width="63%">
Initializes the seeking helper object.

</td>
</tr>
</table> 


## -remarks



To obtain this interface, call <b>CoCreateInstance</b> with CLSID_SeekingPassThru. You can also use the <a href="https://msdn.microsoft.com/d6fccfb4-b256-40aa-b927-84c7a886f631">CreatePosPassThru</a> function in the base class library.



