---
UID: NN:mswmdm.ISCPSession
title: ISCPSession
author: windows-sdk-content
description: The ISCPSession interface provides efficient common state management for multiple operations.A secure content provider (SCP) session is useful when transferring multiple files.
old-location: wmdm\iscpsession.htm
old-project: WMDM
ms.assetid: 4efd8e5a-490b-435b-b34d-7099198891b1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ISCPSession, ISCPSession interface [windows Media Device Manager], ISCPSession interface [windows Media Device Manager],described, ISCPSessionInterface, mswmdm/ISCPSession, wmdm.iscpsession
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	ISCPSession
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISCPSession interface


## -description



The <b>ISCPSession</b> interface provides efficient common state management for multiple operations.

A secure content provider (SCP) session is useful when transferring multiple files. In that case, the session can help SCP do some of the operations only once instead of once for every file transfer. This results in better transfer performance.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSession</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISCPSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da458458-5828-4ab4-8793-d59a07f46569">BeginSession</a>
</td>
<td align="left" width="63%">
Indicates the beginning of a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543004">EndSession</a>
</td>
<td align="left" width="63%">
Indicates the end of a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c725f0ae-1f37-412d-ac2b-0833989d1bd6">GetSecureQuery</a>
</td>
<td align="left" width="63%">
Obtains a secure query object for to the session.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a3eecdb8-55a9-46e3-95d1-0fb9bd59f393">Interfaces for Secure Content Providers</a>
 

 

