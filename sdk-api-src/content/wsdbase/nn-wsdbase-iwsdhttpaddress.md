---
UID: NN:wsdbase.IWSDHttpAddress
title: IWSDHttpAddress
author: windows-sdk-content
description: Provides access to the individual components of an HTTP address.
old-location: ncd\iwsdhttpaddress.htm
old-project: wsdapi
ms.assetid: 79d3570a-56b2-40ad-b3c6-cddc3239da7e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWSDHttpAddress, IWSDHttpAddress interface, IWSDHttpAddress interface,described, ncd.iwsdhttpaddress, wsdbase/IWSDHttpAddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDHttpAddress
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDHttpAddress interface


## -description


Provides access to the individual components of an HTTP address.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDHttpAddress</b> interface inherits from <a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a>. <b>IWSDHttpAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDHttpAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt432961">GetPath</a>
</td>
<td align="left" width="63%">
Gets the URI path for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaf9e918-7d1c-4457-94f8-888a99f07c18">GetSecure</a>
</td>
<td align="left" width="63%">
Retrieves the status on whether TLS secure sessions are enabled for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bad84a6-f321-4275-9787-f6bae83c807e">SetPath</a>
</td>
<td align="left" width="63%">
Sets the URI path for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2b66d0d-51b2-437e-8ceb-a4c95f2f9d6d">SetSecure</a>
</td>
<td align="left" width="63%">
Enables or disables TLS secure sessions for this address.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a>
 

 

