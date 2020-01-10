---
UID: NN:iads.IADsMembers
title: IADsMembers (iads.h)
description: The IADsMembers interface is a dual interface.
old-location: adsi\iadsmembers.htm
tech.root: adsi
ms.assetid: 889e8fc1-61a6-4a3a-82ac-85d41f664149
ms.date: 12/05/2018
ms.keywords: IADsMembers, IADsMembers interface [ADSI], IADsMembers interface [ADSI],described, _ds_iadsmembers, adsi.iadsmembers, iads/IADsMembers
f1_keywords:
- iads/IADsMembers
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsMembers interface


## -description


The <b>IADsMembers</b> interface is a dual interface. It is designed for managing a list of ADSI object references. It is implemented to support group membership for individual accounts. It can be used to manage a collection of ADSI objects belonging to a group. To access the collection of group members, use the  <a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup::get_Members</a> property method implemented by the ADSI group object.

The <b>IADsMembers</b> interface serves a slightly different purpose from the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a> and  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interfaces, which also works with a set of data or objects. <b>IADsCollection</b> manages sets of arbitrary data elements that are not object references, whereas <b>IADsContainer</b> manages objects that are part of the directory tree structure or the network topology.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsMembers</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsMembers</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum">get__NewEnum</a>
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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsmembers-property-methods">Count</a>


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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsmembers-property-methods">Filter</a>


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




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup::get_Members</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsmembers-property-methods">IADsMembers Property
    Methods</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

