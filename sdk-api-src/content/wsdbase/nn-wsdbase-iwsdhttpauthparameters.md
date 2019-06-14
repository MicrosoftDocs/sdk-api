---
UID: NN:wsdbase.IWSDHttpAuthParameters
title: IWSDHttpAuthParameters (wsdbase.h)
author: windows-sdk-content
description: Use this interface to retrieve the access token or authorization scheme used during the authentication of a client.
old-location: ncd\iwsdhttpauthparameters.htm
tech.root: WsdApi
ms.assetid: 77AB4D22-55F2-4DF6-8E83-718BFB88841A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDHttpAuthParameters, IWSDHttpAuthParameters interface, IWSDHttpAuthParameters interface,described, ncd.iwsdhttpauthparameters, wsdbase/IWSDHttpAuthParameters
ms.topic: interface
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - Wsdbase.h
api_name:
 - IWSDHttpAuthParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDHttpAuthParameters interface


## -description


Use this interface to retrieve the access token or authorization scheme used during the authentication of a client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDHttpAuthParameters</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDHttpAuthParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDHttpAuthParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpauthparameters-getauthtype">GetAuthType</a>
</td>
<td align="left" width="63%">
Retrieves the HTTP authentication scheme that was used for the authentication of the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdhttpauthparameters-getclientaccesstoken">GetClientAccessToken</a>
</td>
<td align="left" width="63%">
Retrieves the client access token that can be used to either authenticate or impersonate the client.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

