---
UID: NN:wpcapi.IWPCProviderConfig
title: IWPCProviderConfig (wpcapi.h)
description: Exposes configuration methods that are implemented by third parties.
helpviewer_keywords: ["IWPCProviderConfig","IWPCProviderConfig interface","IWPCProviderConfig interface","described","parcon.iwpcproviderconfig","wpcapi/IWPCProviderConfig"]
old-location: parcon\iwpcproviderconfig.htm
tech.root: parcon
ms.assetid: 008786aa-72ef-4591-8826-01176d3e3fba
ms.date: 12/05/2018
ms.keywords: IWPCProviderConfig, IWPCProviderConfig interface, IWPCProviderConfig interface,described, parcon.iwpcproviderconfig, wpcapi/IWPCProviderConfig
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWPCProviderConfig
 - wpcapi/IWPCProviderConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderConfig
---

# IWPCProviderConfig interface


## -description

Exposes configuration methods that are implemented by third parties. Parental Controls uses the CLSID from the provider's ConfigCLSID registry details to call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>. The <b>CLSCTX_LOCAL_SERVER</b> flag is used when creating an instance of the class.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCProviderConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWPCProviderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCProviderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wpcapi/nf-wpcapi-iwpcproviderconfig-configure">Configure</a>
</td>
<td align="left" width="63%">
Called for the current provider when you click a user tile in the Parental Controls Control Panel. This method allows for changes to the configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wpcapi/nf-wpcapi-iwpcproviderconfig-getusersummary">GetUserSummary</a>
</td>
<td align="left" width="63%">
Retrieves the information for each user by using the Parental Controls Control Panel.

</td>
</tr>
</table>