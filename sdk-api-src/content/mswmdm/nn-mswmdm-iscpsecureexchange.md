---
UID: NN:mswmdm.ISCPSecureExchange
title: ISCPSecureExchange
author: windows-sdk-content
description: The ISCPSecureExchange interface is used to exchange secured content and rights associated with content. The secure content provider implements this interface and secure Windows Media Device Manager implementations call its methods.
old-location: wmdm\iscpsecureexchange.htm
tech.root: WMDM
ms.assetid: 8c61e1a0-18fc-4ae9-881a-0362166012d9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISCPSecureExchange, ISCPSecureExchange interface [windows Media Device Manager], ISCPSecureExchange interface [windows Media Device Manager],described, ISCPSecureExchangeInterface, mswmdm/ISCPSecureExchange, wmdm.iscpsecureexchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - mswmdm.h
api_name:
 - ISCPSecureExchange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCPSecureExchange interface


## -description



The <b>ISCPSecureExchange</b> interface is used to exchange secured content and rights associated with content. The secure content provider implements this interface and secure Windows Media Device Manager implementations call its methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureExchange</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISCPSecureExchange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureExchange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/825539e4-9162-40b7-bae0-336e728fb34e">ObjectData</a>
</td>
<td align="left" width="63%">
Transfers a block of object data to Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a7a6de0-ab37-4764-8feb-82676e1e62ab">TransferComplete</a>
</td>
<td align="left" width="63%">
Called by Windows Media Device Manager to signal the end of a secure transfer of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97b55751-b45e-4204-87e2-1e653d55a718">TransferContainerData</a>
</td>
<td align="left" width="63%">
Transfers container file data to the secure content provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/815fd9b9-2186-40e2-8d72-e6bf91fd45c9">ISCPSecureExchange2 Interface</a>



<a href="https://msdn.microsoft.com/2617a6af-c91d-4416-8bef-fe69404e7c3f">ISCPSecureExchange3 Interface</a>



<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

