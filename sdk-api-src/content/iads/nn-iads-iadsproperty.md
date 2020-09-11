---
UID: NN:iads.IADsProperty
title: IADsProperty (iads.h)
description: The IADsProperty interface is designed to manage a single attribute definition for a schema class object.
helpviewer_keywords: ["IADsProperty","IADsProperty interface [ADSI]","IADsProperty interface [ADSI]","described","_ds_iadsproperty","adsi.iadsproperty","iads/IADsProperty"]
old-location: adsi\iadsproperty.htm
tech.root: adsi
ms.assetid: ebf03974-371b-4bf4-91b4-f137339bd784
ms.date: 12/05/2018
ms.keywords: IADsProperty, IADsProperty interface [ADSI], IADsProperty interface [ADSI],described, _ds_iadsproperty, adsi.iadsproperty, iads/IADsProperty
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
 - IADsProperty
 - iads/IADsProperty
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
 - IADsProperty
---

# IADsProperty interface


## -description

The <b>IADsProperty</b> interface is designed to manage a single 
    attribute definition for a schema class object. An attribute definition specifies the minimum and maximum values 
    of a property, its syntax, and whether the property supports multiple values. Other interfaces involved in schema 
    management include <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsclass">IADsClass</a> and 
    <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssyntax">IADsSyntax</a>.

The <b>IADsProperty</b> interface exposes methods to describe a 
    property by name, syntax, value ranges, and any other defined attributes. A property can have multiple names 
    associated with it, but providers must  ensure that each name is unique.

Use the <b>IADsProperty</b> interface to determine at run time 
    the attribute definition of a property supported by a directory service object.
<p class="proch"><b>To determine the attribute definition at run time</b>
<ol>
<li>Bind to the schema class object of the ADSI object.</li>
<li>Enumerate mandatory or optional attributes accessible from the schema class object. Skip this step if you 
     know that the object supports the attribute of your interest.</li>
<li>Bind to the schema container of the schema class object you obtained in first step.</li>
<li>Retrieve the attribute definition object of the property of interest from the schema container.</li>
<li>Examine the attribute definition of the property. You may have to also inspect the syntax object.</li>
</ol>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsProperty</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
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
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsproperty-qualifiers">Qualifiers</a>
</td>
<td align="left" width="63%">
Optional additional provider-specific constraints on this property.

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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsProperty</b> interface has these properties.
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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsproperty-property-methods">MaxRange</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Upper limit of values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsproperty-property-methods">MinRange</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Lower limit of values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsproperty-property-methods">MultiValued</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Whether or not this is a property that supports multiple values.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsproperty-property-methods">OID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Directory-specific object identifier.

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
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsproperty-property-methods">Syntax</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Relative path of the syntax object.

</td>
</tr>
</table>

## -remarks

The <b>IADsProperty</b> interface methods can add new 
    attributes and property objects to a provider-specific implementation.


#### Examples

The following code example shows the procedure above for applying the 
     <b>IADsProperty</b> interface to determine attribute 
     definitions of a property.


```vb
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer

On Error GoTo Cleanup
 
' Step 1
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
 
' Step 2
' Skip it, assuming the "Owner" attribute is supported by obj.
' For the computer object in this example, it is indeed one of 
' the supported optional properties.
 
' Step 3
Set sc = GetObject(cl.Parent)
 
' Step 4
Set pr = sc.GetObject("Property","Owner")
 
' Step 5
MsgBox "Attribute: " & pr.Name
MsgBox "Syntax:    " & pr.Syntax
If pr.Multivalued = True Then
    MsgBox "The Owner attribute has multiple values."
Else
    MsgBox "The Owner attribute has a single value."
End If
 
' To further examine the syntax
Set sy = GetObject(sc.AdsPath & "/" & pr.Syntax)
MsgBox "Syntax object: " & sy.Name & " of OleAutoDataType: " _
       & sy.OleAutoDataType

Cleanup:
    If (Err.Number <> 0 ) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsclass">IADsClass</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

