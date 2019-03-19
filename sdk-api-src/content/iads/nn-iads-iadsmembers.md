---
UID: NN:iads.IADsMembers
title: IADsMembers (iads.h)
author: windows-sdk-content
description: The IADsMembers interface is a dual interface.
old-location: adsi\iadsmembers.htm
tech.root: adsi
ms.assetid: 889e8fc1-61a6-4a3a-82ac-85d41f664149
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsMembers, IADsMembers interface [ADSI], IADsMembers interface [ADSI],described, _ds_iadsmembers, adsi.iadsmembers, iads/IADsMembers
ms.topic: interface
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsMembers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsMembers interface


## -description


The <b>IADsMembers</b> interface is a dual interface. It is designed for managing a list of ADSI object references. It is implemented to support group membership for individual accounts. It can be used to manage a collection of ADSI objects belonging to a group. To access the collection of group members, use the  <a href="https://msdn.microsoft.com/a8aa88d4-4695-47bc-bf7f-a17236a5671c">IADsGroup::get_Members</a> property method implemented by the ADSI group object.

The <b>IADsMembers</b> interface serves a slightly different purpose from the  <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> and  <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interfaces, which also works with a set of data or objects. <b>IADsCollection</b> manages sets of arbitrary data elements that are not object references, whereas <b>IADsContainer</b> manages objects that are part of the directory tree structure or the network topology.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsMembers</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IADsMembers</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsMembers</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a65794c-2407-4267-bc02-d84a134f6bf4">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsMembers</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ed4e98e5-053c-4d3b-bcd0-3add96bbe120">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ed4e98e5-053c-4d3b-bcd0-3add96bbe120">Filter</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the filter for selection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/a8aa88d4-4695-47bc-bf7f-a17236a5671c">IADsGroup::get_Members</a>



<a href="https://msdn.microsoft.com/ed4e98e5-053c-4d3b-bcd0-3add96bbe120">IADsMembers Property
    Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

