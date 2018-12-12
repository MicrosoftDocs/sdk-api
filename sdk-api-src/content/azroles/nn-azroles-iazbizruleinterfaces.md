---
UID: NN:azroles.IAzBizRuleInterfaces
title: IAzBizRuleInterfaces
author: windows-sdk-content
description: Provides methods and properties used to manage a list of IDispatch interfaces that can be called by business rule (BizRule) scripts.
old-location: security\iazbizruleinterfaces.htm
tech.root: secauthz
ms.assetid: 96cc0e45-ddd5-4ab0-9243-5f2046e48f78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAzBizRuleInterfaces, IAzBizRuleInterfaces interface [Security], IAzBizRuleInterfaces interface [Security],described, azroles/IAzBizRuleInterfaces, security.iazbizruleinterfaces
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzBizRuleInterfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzBizRuleInterfaces interface


## -description


The <b>IAzBizRuleInterfaces</b> interface provides methods and properties used to manage a list of <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interfaces that can be called by business rule (BizRule) scripts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzBizRuleInterfaces</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzBizRuleInterfaces</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzBizRuleInterfaces</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/063492b9-9970-4605-84f5-d8b80afc719b">AddInterface</a>
</td>
<td align="left" width="63%">
Adds the specified interface to the list of interfaces available to BizRule scripts.  To add the specified interface, AzMan calls the  <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">AddNamedItem</a> method of the <a href="d8acee11-7f0d-4999-b97a-66774af16f71">IActiveScript</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91822c84-4daa-4d3c-bbe2-9ceb7fc642b2">AddInterfaces</a>
</td>
<td align="left" width="63%">
Adds the specified interfaces to the list of interfaces available to BizRule scripts. To add the specified interfaces, AzMan calls the <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">AddNamedItem</a> method of the <a href="d8acee11-7f0d-4999-b97a-66774af16f71">IActiveScript</a> interface once for each specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5d12529-6ce8-4189-949b-210d8ec84084">GetInterfaceValue</a>
</td>
<td align="left" width="63%">
Gets the ID and flags of the interface that corresponds to the specified interface name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/398e4151-aeda-48d0-b6f5-e0ea749d0720">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified interface from the list of interfaces available to BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05e0d7af-5b09-4112-9229-862197a9895b">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all interfaces from the list of interfaces available to BizRule scripts.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzBizRuleInterfaces</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f6838790-2223-4ae8-9cee-9d881d071ba0">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of interfaces in the list of interfaces available to BizRule scripts.

</td>
</tr>
</table> 

