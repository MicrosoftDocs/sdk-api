---
UID: NN:wpcapi.IWPCProviderState
title: IWPCProviderState (wpcapi.h)
description: Exposes provider state methods that are implemented by third parties.
old-location: parcon\iwpcproviderstate.htm
tech.root: parcon
ms.assetid: a5cd14df-8e64-4f34-801c-9901c7d215f9
ms.date: 12/05/2018
ms.keywords: IWPCProviderState, IWPCProviderState interface, IWPCProviderState interface,described, parcon.iwpcproviderstate, wpcapi/IWPCProviderState
f1_keywords:
- wpcapi/IWPCProviderState
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
req.idl: Wpcprovider.idl
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
- IWPCProviderState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWPCProviderState interface


## -description


Exposes provider state methods that are implemented by third parties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCProviderState</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWPCProviderState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCProviderState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwpcproviderstate-disable">Disable</a>
</td>
<td align="left" width="63%">
Notifies the third-party application that it is not the current provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wpcapi/nf-wpcapi-iwpcproviderstate-enable">Enable</a>
</td>
<td align="left" width="63%">
Notifies the third-party application that it has been selected as the new current provider.

</td>
</tr>
</table> 

