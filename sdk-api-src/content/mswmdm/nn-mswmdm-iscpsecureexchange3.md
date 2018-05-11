---
UID: NN:mswmdm.ISCPSecureExchange3
title: ISCPSecureExchange3
author: windows-driver-content
description: The ISCPSecureExchange3 interface extends ISCPSecureExchange2 by providing improved data exchange performance, and a transfer-complete callback method.
old-location: wmdm\iscpsecureexchange3.htm
old-project: WMDM
ms.assetid: 2617a6af-c91d-4416-8bef-fe69404e7c3f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISCPSecureExchange3, ISCPSecureExchange3 interface [windows Media Device Manager], ISCPSecureExchange3 interface [windows Media Device Manager],described, ISCPSecureExchange3Interface, mswmdm/ISCPSecureExchange3, wmdm.iscpsecureexchange3
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	ISCPSecureExchange3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISCPSecureExchange3 interface


## -description



The <b>ISCPSecureExchange3</b> interface extends <b>ISCPSecureExchange2</b> by providing improved data exchange performance, and a transfer-complete callback method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureExchange3</b> interface inherits from <a href="https://msdn.microsoft.com/815fd9b9-2186-40e2-8d72-e6bf91fd45c9">ISCPSecureExchange2</a>. <b>ISCPSecureExchange3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureExchange3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62122415-b45b-436e-8c5f-28be759ba8c0">GetObjectDataOnClearChannel</a>
</td>
<td align="left" width="63%">
Retrieves the object data on a clear channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5144d290-444d-4a8c-ad3d-292bb8168e99">TransferCompleteForDevice</a>
</td>
<td align="left" width="63%">
Indicates that the data transfer has completed for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aac0fc79-4615-442f-8c08-06addf40c799">TransferContainerDataOnClearChannel</a>
</td>
<td align="left" width="63%">
Transfers the container data on a clear channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8c61e1a0-18fc-4ae9-881a-0362166012d9">ISCPSecureExchange Interface</a>



<a href="https://msdn.microsoft.com/815fd9b9-2186-40e2-8d72-e6bf91fd45c9">ISCPSecureExchange2 Interface</a>



<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

