---
UID: NN:strmif.IGetCapabilitiesKey
title: IGetCapabilitiesKey (strmif.h)
author: windows-sdk-content
description: The IGetCapabilitiesKey interface enables an application to retrieve the capabilities of a software or hardware codec from the registry, without creating an instance of the encoder filter.
old-location: dshow\igetcapabilitieskey.htm
tech.root: DirectShow
ms.assetid: 97a9112f-7b7b-4a7e-8f40-bdb148d413c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGetCapabilitiesKey, IGetCapabilitiesKey interface [DirectShow], IGetCapabilitiesKey interface [DirectShow],described, IGetCapabilitiesKeyInterface, dshow.igetcapabilitieskey, strmif/IGetCapabilitiesKey
ms.topic: interface
f1_keywords: 
 - "strmif/IGetCapabilitiesKey"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IGetCapabilitiesKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGetCapabilitiesKey interface


## -description



The <b>IGetCapabilitiesKey</b> interface enables an application to retrieve the capabilities of a software or hardware codec from the registry, without creating an instance of the encoder filter. The moniker for the codec filter exposes this interface. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetCapabilitiesKey</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetCapabilitiesKey</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetCapabilitiesKey</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey">GetCapabilitiesKey</a>
</td>
<td align="left" width="63%">
Gets a registry key that contains the capabilities information for the codec.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

