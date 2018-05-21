---
UID: NN:certcli.ICertGetConfig
title: ICertGetConfig
author: windows-driver-content
description: Provides functionality for retrieving the public configuration data (specified during client setup) for a Certificate Services server.
old-location: security\icertgetconfig.htm
old-project: SecCrypto
ms.assetid: 753d1527-1863-41af-9715-2c1fe138e67d
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ICertGetConfig, ICertGetConfig interface [Security], ICertGetConfig interface [Security],described, certcli/ICertGetConfig, security.icertgetconfig
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509EnrollmentAuthFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certcli.dll
api_name:
-	ICertGetConfig
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertGetConfig interface


## -description


The <b>ICertGetConfig</b> interface provides functionality for retrieving  the public  configuration data (specified during client setup) for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Services</a> server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertGetConfig</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertGetConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5935bf37-4a4a-4c0f-ae3f-bd76f97d0d9a">GetConfig</a>
</td>
<td align="left" width="63%">
Retrieves the configuration string for a Certificate Services server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6bac5961-f9cc-4859-affa-aa7ed152ebfa">ICertConfig2</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

