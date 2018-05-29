---
UID: NN:mswmdm.IMDServiceProvider2
title: IMDServiceProvider2
author: windows-sdk-content
description: The IMDServiceProvider2 interface extends the IMDServiceProvider interface by providing a way of obtaining IMDSPDevice object(s) for a given device path name. The device path name comes from the Plug and Play (PnP) subsystem.
old-location: wmdm\imdserviceprovider2.htm
old-project: WMDM
ms.assetid: d9ffaea8-5616-4bc2-a27c-8b77ea177b6b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMDServiceProvider2, IMDServiceProvider2 interface [windows Media Device Manager], IMDServiceProvider2 interface [windows Media Device Manager],described, IMDServiceProvider2Interface, mswmdm/IMDServiceProvider2, wmdm.imdserviceprovider2
ms.prod: windows
ms.technology: windows-sdk
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
-	IMDServiceProvider2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDServiceProvider2 interface


## -description



The <b>IMDServiceProvider2</b> interface extends the <a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider</a> interface by providing a way of obtaining <a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a> object(s) for a given device path name. The device path name comes from the Plug and Play (PnP) subsystem.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDServiceProvider2</b> interface inherits from <a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider</a>. <b>IMDServiceProvider2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDServiceProvider2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f724ef14-c572-41ca-a56b-fde85d7620e0">CreateDevice</a>
</td>
<td align="left" width="63%">
Creates devices by using the device path.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

