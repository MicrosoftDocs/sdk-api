---
UID: NN:mswmdm.ISCPSecureExchange2
title: ISCPSecureExchange2
author: windows-driver-content
description: The ISCPSecureExchange2 interface extends ISCPSecureExchange by providing a new version of the TransferContainerData method.
old-location: wmdm\iscpsecureexchange2.htm
old-project: WMDM
ms.assetid: 815fd9b9-2186-40e2-8d72-e6bf91fd45c9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ISCPSecureExchange2, ISCPSecureExchange2 interface [windows Media Device Manager], ISCPSecureExchange2 interface [windows Media Device Manager], described, ISCPSecureExchange2Interface, mswmdm/ISCPSecureExchange2, wmdm.iscpsecureexchange2
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
-	ISCPSecureExchange2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISCPSecureExchange2 interface


## -description



The <b>ISCPSecureExchange2</b> interface extends <a href="https://msdn.microsoft.com/8c61e1a0-18fc-4ae9-881a-0362166012d9">ISCPSecureExchange</a> by providing a new version of the <b>TransferContainerData</b> method. <b>TransferContainerData2</b> accepts a progress callback on which the secure content provider can send progress notifications for any of the steps it needs to carry out.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureExchange2</b> interface inherits from <a href="https://msdn.microsoft.com/8c61e1a0-18fc-4ae9-881a-0362166012d9">ISCPSecureExchange</a>. <b>ISCPSecureExchange2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureExchange2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e130da3-2bef-4ff0-870c-31ac4c3767e5">TransferContainerData2</a>
</td>
<td align="left" width="63%">
Transfers container file data to the secure content provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8c61e1a0-18fc-4ae9-881a-0362166012d9">ISCPSecureExchange Interface</a>



<a href="https://msdn.microsoft.com/2617a6af-c91d-4416-8bef-fe69404e7c3f">ISCPSecureExchange3 Interface</a>



<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

