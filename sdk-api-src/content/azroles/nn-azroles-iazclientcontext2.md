---
UID: NN:azroles.IAzClientContext2
title: IAzClientContext2
author: windows-sdk-content
description: Inherits from the IAzClientContext interface and implements new methods that manipulate the client context.
old-location: security\iazclientcontext2.htm
old-project: SecAuthZ
ms.assetid: 8e922370-18e3-481c-93f2-9a56d7898ba7
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IAzClientContext2, IAzClientContext2 interface [Security], IAzClientContext2 interface [Security],described, azroles/IAzClientContext2, security.iazclientcontext2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzClientContext2
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext2 interface


## -description


The <b>IAzClientContext2</b> interface inherits from the <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> interface and implements new methods that manipulate the client context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext2</b> interface inherits from <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a>. <b>IAzClientContext2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzClientContext2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ad7c7df-0bdd-4ea1-9a9e-98323b82c0b0">AddApplicationGroups</a>
</td>
<td align="left" width="63%">
Adds the specified array of existing <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> objects to the client context object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa81e935-1207-44dd-85cb-215f754575fe">AddRoles</a>
</td>
<td align="left" width="63%">
Adds the specified array of existing <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> objects to the client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac437686-fefb-413e-9f53-eed6c1df5798">AddStringSids</a>
</td>
<td align="left" width="63%">
Adds an array of string representations of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) to the client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/496dd834-37d9-41f6-a552-39c558dd60b3">GetAssignedScopesPage</a>
</td>
<td align="left" width="63%">
Retrieves a list of the scopes in which the client represented by the current <b>IAzClientContext2</b> object is assigned to at least one role.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3d06e240-10d9-4d58-baae-c3d2a38ac556">LDAPQueryDN</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the domain name of the directory object to be used during evaluation of LDAP query groups.

</td>
</tr>
</table> 

