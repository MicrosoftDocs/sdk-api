---
UID: NN:iads.IADsGroup
title: IADsGroup (iads.h)
author: windows-sdk-content
description: Manages group membership data in a directory service.
old-location: adsi\iadsgroup.htm
tech.root: adsi
ms.assetid: dbf0c424-e906-4a72-a369-81bf96275bbc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsGroup, IADsGroup interface [ADSI], IADsGroup interface [ADSI],described, _ds_iadsgroup, adsi.iadsgroup, iads/IADsGroup
ms.topic: interface
f1_keywords: 
 - "iads/IADsGroup"
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
 - IADsGroup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsGroup interface


## -description


The <b>IADsGroup</b> interface is a dual interface that inherits from  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It manages group membership data in a directory service. It enables you to get member objects, test if a given object belongs to the group, and to add, or remove, an object to, or from, the group.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsGroup</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsgroup-add">Add</a>
</td>
<td align="left" width="63%">
Adds an object to a group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-get">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getex">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfoex">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsgroup-ismember">IsMember</a>
</td>
<td align="left" width="63%">
Verifies membership.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsgroup-members">Members</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a> interface on the members object that is the collection of ADSI objects that represent the members of this group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-put">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-putex">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsgroup-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an object from a group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-setinfo">SetInfo</a>
</td>
<td align="left" width="63%">
Persists the changes on this object to the underlying directory store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsGroup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">AdsPath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's ADsPath that uniquely identifies this object from all others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Class</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the object's schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsgroup-property-methods">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the description of the group membership.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the GUID of the object as stored in the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's relative name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string for the parent of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Schema</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string to the schema class object for this object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup
    Property Methods</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

