---
UID: NN:azroles.IAzClientContext2
title: IAzClientContext2
author: windows-sdk-content
description: Inherits from the IAzClientContext interface and implements new methods that manipulate the client context.
old-location: security\iazclientcontext2.htm
old-project: secauthz
ms.assetid: 8e922370-18e3-481c-93f2-9a56d7898ba7
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: IAzClientContext2, IAzClientContext2 interface [Security], IAzClientContext2 interface [Security],described, azroles/IAzClientContext2, security.iazclientcontext2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext2
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzClientContext2 interface


## -description


The <b>IAzClientContext2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/Aa377837(v=VS.85).aspx">IAzClientContext</a> interface and implements new methods that manipulate the client context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzClientContext2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa377837(v=VS.85).aspx">IAzClientContext</a>. <b>IAzClientContext2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377842(v=VS.85).aspx">AddApplicationGroups</a>
</td>
<td align="left" width="63%">
Adds the specified array of existing <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> objects to the client context object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377846(v=VS.85).aspx">AddRoles</a>
</td>
<td align="left" width="63%">
Adds the specified array of existing <a href="https://msdn.microsoft.com/en-us/library/Aa377917(v=VS.85).aspx">IAzRole</a> objects to the client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377850(v=VS.85).aspx">AddStringSids</a>
</td>
<td align="left" width="63%">
Adds an array of string representations of <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">security identifiers</a> (SIDs) to the client context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377854(v=VS.85).aspx">GetAssignedScopesPage</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa377857(v=VS.85).aspx">LDAPQueryDN</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the domain name of the directory object to be used during evaluation of LDAP query groups.

</td>
</tr>
</table> 

