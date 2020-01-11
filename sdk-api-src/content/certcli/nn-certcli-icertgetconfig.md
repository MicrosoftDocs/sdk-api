---
UID: NN:certcli.ICertGetConfig
title: ICertGetConfig (certcli.h)
description: Provides functionality for retrieving the public configuration data (specified during client setup) for a Certificate Services server.
old-location: security\icertgetconfig.htm
tech.root: SecCrypto
ms.assetid: 753d1527-1863-41af-9715-2c1fe138e67d
ms.date: 12/05/2018
ms.keywords: ICertGetConfig, ICertGetConfig interface [Security], ICertGetConfig interface [Security],described, certcli/ICertGetConfig, security.icertgetconfig
f1_keywords:
- certcli/ICertGetConfig
dev_langs:
- c++
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Certcli.dll
api_name:
- ICertGetConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertGetConfig interface


## -description


The <b>ICertGetConfig</b> interface provides functionality for retrieving  the public  configuration data (specified during client setup) for a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Services</a> server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertGetConfig</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertGetConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICertGetConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nf-certcli-icertgetconfig-getconfig">GetConfig</a>
</td>
<td align="left" width="63%">
Retrieves the configuration string for a Certificate Services server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certcli/nn-certcli-icertconfig2">ICertConfig2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

