---
UID: NN:wincodecsdk.IWICStreamProvider
title: IWICStreamProvider (wincodecsdk.h)
description: Exposes methods for a stream provider.
old-location: wic\_wic_codec_iwicstreamprovider.htm
tech.root: wic
ms.assetid: fdcaf668-a5c3-4852-8bc9-5535f0756592
ms.date: 12/05/2018
ms.keywords: IWICStreamProvider, IWICStreamProvider interface [Windows Imaging Component], IWICStreamProvider interface [Windows Imaging Component],described, _wic_codec_iwicstreamprovider, wic._wic_codec_iwicstreamprovider, wincodecsdk/IWICStreamProvider
f1_keywords:
- wincodecsdk/IWICStreamProvider
dev_langs:
- c++
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.dll
api_name:
- IWICStreamProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICStreamProvider interface


## -description


Exposes methods for a stream provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICStreamProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICStreamProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICStreamProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicstreamprovider-getpersistoptions">GetPersistOptions</a>
</td>
<td align="left" width="63%">
Gets the persist options used when initializing the component with a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicstreamprovider-getpreferredvendorguid">GetPreferredVendorGUID</a>
</td>
<td align="left" width="63%">
Gets the preferred vendor GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicstreamprovider-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets the stream held by the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicstreamprovider-refreshstream">RefreshStream</a>
</td>
<td align="left" width="63%">
Informs the component that the content of the stream it's holding onto may have changed. The component should respond by dirtying any cached information from the stream.

</td>
</tr>
</table> 

