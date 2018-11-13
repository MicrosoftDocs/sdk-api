---
UID: NN:certcli.ICertGetConfig
title: ICertGetConfig
author: windows-sdk-content
description: Provides functionality for retrieving the public configuration data (specified during client setup) for a Certificate Services server.
old-location: security\icertgetconfig.htm
tech.root: seccrypto
ms.assetid: 753d1527-1863-41af-9715-2c1fe138e67d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ICertGetConfig, ICertGetConfig interface [Security], ICertGetConfig interface [Security],described, certcli/ICertGetConfig, security.icertgetconfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertGetConfig interface


## -description


The <b>ICertGetConfig</b> interface provides functionality for retrieving  the public  configuration data (specified during client setup) for a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Services</a> server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertGetConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertGetConfig</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa385028(v=VS.85).aspx">GetConfig</a>
</td>
<td align="left" width="63%">
Retrieves the configuration string for a Certificate Services server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383272(v=VS.85).aspx">ICertConfig2</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

