---
UID: NN:wpcapi.IWPCProviderSupport
title: IWPCProviderSupport (wpcapi.h)
description: Exposes methods that allow third-party providers to query the currently enabled provider.helpviewer_keywords: ["IWPCProviderSupport","IWPCProviderSupport interface","IWPCProviderSupport interface","described","parcon.iwpcprovidersupport","wpcapi/IWPCProviderSupport"]
old-location: parcon\iwpcprovidersupport.htm
tech.root: parcon
ms.assetid: 5c2a793b-d136-4d03-9e46-b24009af2c7d
ms.date: 12/05/2018
ms.keywords: IWPCProviderSupport, IWPCProviderSupport interface, IWPCProviderSupport interface,described, parcon.iwpcprovidersupport, wpcapi/IWPCProviderSupport
f1_keywords:
- wpcapi/IWPCProviderSupport
dev_langs:
- c++
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wpcapi.h
api_name:
- IWPCProviderSupport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWPCProviderSupport interface


## -description


Exposes methods that allow third-party providers to query the currently enabled provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCProviderSupport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWPCProviderSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCProviderSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwpcprovidersupport-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the current provider.

</td>
</tr>
</table> 

