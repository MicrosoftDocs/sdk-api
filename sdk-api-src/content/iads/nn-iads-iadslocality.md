---
UID: NN:iads.IADsLocality
title: IADsLocality (iads.h)
description: The IADsLocality interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsLocality","IADsLocality interface [ADSI]","IADsLocality interface [ADSI]","described","_ds_iadslocality","adsi.iadslocality","iads/IADsLocality"]
old-location: adsi\iadslocality.htm
tech.root: adsi
ms.assetid: fec0c8c2-b17f-49a0-9c97-260c98e71604
ms.date: 12/05/2018
ms.keywords: IADsLocality, IADsLocality interface [ADSI], IADsLocality interface [ADSI],described, _ds_iadslocality, adsi.iadslocality, iads/IADsLocality
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsLocality
 - iads/IADsLocality
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsLocality
---

# IADsLocality interface


## -description

The <b>IADsLocality</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to represent the geographical location, or region, of a directory entity. This interface is one of several that provide support for directory services to organize accounts by country/region, locality (state/city/region), organization (company), or organizational unit (department). This interface manages locality, the  <a href="/windows/desktop/api/iads/nn-iads-iadso">IADsO</a> interface manages organization, and the  <a href="/windows/desktop/api/iads/nn-iads-iadsou">IADsOU</a> interface manages the organization unit.
   

When a directory service provides hierarchical groupings of directory entries by country/region, locality, organization, or organization unit, you can use this and the related interfaces to expand the directory tree accordingly. In this case, the <b>IADsLocality</b> interface is implemented by a locality object that implements the <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsLocality</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsLocality</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsLocality</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iads-get">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iads-getex">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iads-put">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iads-putex">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">SetInfo</a>
</td>
<td align="left" width="63%">
Persists the changes on this object to the underlying directory store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsLocality</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/ADSI/iads-property-methods">AdsPath</a>


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

<a href="/windows/desktop/ADSI/iads-property-methods">Class</a>


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

<a href="/windows/desktop/ADSI/iadslocality-property-methods">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the description of the geographical region as represented by this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/ADSI/iads-property-methods">GUID</a>


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

<a href="/windows/desktop/ADSI/iadslocality-property-methods">LocalityName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the name of this region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/ADSI/iads-property-methods">Name</a>


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

<a href="/windows/desktop/ADSI/iads-property-methods">Parent</a>


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

<a href="/windows/desktop/ADSI/iadslocality-property-methods">PostalAddress</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the main post office address of this region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/ADSI/iads-property-methods">Schema</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string to the schema class object for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/ADSI/iadslocality-property-methods">SeeAlso</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets any other information relevant to this region.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadslocality-property-methods">IADsLocality Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadso">IADsO</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsou">IADsOU</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>