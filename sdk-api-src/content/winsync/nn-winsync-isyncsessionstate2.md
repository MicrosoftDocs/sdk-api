---
UID: NN:winsync.ISyncSessionState2
title: ISyncSessionState2
author: windows-driver-content
description: Represents additional information about the current synchronization session.
old-location: winsync\isyncsessionstate2.htm
old-project: winsync
ms.assetid: c98e675f-48f4-4ffa-bc81-18a58edd8c34
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISyncSessionState2, ISyncSessionState2 interface [Windows Sync], ISyncSessionState2 interface [Windows Sync],described, winsync.isyncsessionstate2, winsync/ISyncSessionState2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Winsync.h
api_name:
-	ISyncSessionState2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncSessionState2 interface


## -description


Represents additional information about the current synchronization session.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncSessionState2</b> interface inherits from <a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState</a>. <b>ISyncSessionState2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncSessionState2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74b263c0-ef6a-4159-9ea2-301b7064331d">GetSessionErrorStatus</a>
</td>
<td align="left" width="63%">
Gets the error value that indicates why the synchronization session failed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcbfcc13-5a8f-4062-baef-899f81413768">SetProviderWithError</a>
</td>
<td align="left" width="63%">
Indicates which provider caused synchronization to fail.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncSessionState2</b> object can be obtained by passing <b>IID_ISyncSessionState2</b> to the <b>QueryInterface</b> method of an <b>ISyncSessionState</b> object.




## -see-also




<a href="https://msdn.microsoft.com/9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e">ISyncSessionState Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

