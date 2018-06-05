---
UID: NN:identityprovider.IIdentityAdvise
title: IIdentityAdvise
author: windows-sdk-content
description: Allows an identity provider to notify a calling application when an identity is updated.
old-location: security\iidentityadvise.htm
old-project: SecAuthN
ms.assetid: fa348d46-bcd2-4009-89d6-11e738d4a82b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IIdentityAdvise, IIdentityAdvise interface [Security], IIdentityAdvise interface [Security],described, identityprovider/IIdentityAdvise, identitystore/IIdentityAdvise, security.iidentityadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: identityprovider.h
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
tech.root: 
req.typenames: IDENTITY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	IdentityProvider.h
-	Identitystore.h
api_name:
-	IIdentityAdvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIdentityAdvise interface


## -description


The <b>IIdentityAdvise</b> interface allows an identity provider to notify a calling application when an identity is updated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIdentityAdvise</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIdentityAdvise</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIdentityAdvise</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c41ca389-eac9-4c74-b0e7-950cd21f2199">IdentityUpdated</a>
</td>
<td align="left" width="63%">
Is called by an identity provider to notify a calling application that an identity event occurred.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>



<a href="https://msdn.microsoft.com/fcac9d30-64ed-4746-aacc-ee659c2b2642">IIdentityProvider::Advise</a>
 

 

