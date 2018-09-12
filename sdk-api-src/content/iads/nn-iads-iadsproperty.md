---
UID: NN:iads.IADsProperty
title: IADsProperty
author: windows-sdk-content
description: The IADsProperty interface is designed to manage a single attribute definition for a schema class object.
old-location: adsi\iadsproperty.htm
tech.root: ADSI
ms.assetid: ebf03974-371b-4bf4-91b4-f137339bd784
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsProperty, IADsProperty interface [ADSI], IADsProperty interface [ADSI],described, _ds_iadsproperty, adsi.iadsproperty, iads/IADsProperty
ms.prod: windows
ms.technology: windows-sdk
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
 - IADsProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsProperty interface


## -description


The <b>IADsProperty</b> interface is designed to manage a single 
    attribute definition for a schema class object. An attribute definition specifies the minimum and maximum values 
    of a property, its syntax, and whether the property supports multiple values. Other interfaces involved in schema 
    management include <a href="https://msdn.microsoft.com/690b0c96-6319-42d8-8b0e-c43f46f91031">IADsClass</a> and 
    <a href="https://msdn.microsoft.com/1ff8703f-b89d-435d-81af-e5c9a2dc01e2">IADsSyntax</a>.

The <b>IADsProperty</b> interface exposes methods to describe a 
    property by name, syntax, value ranges, and any other defined attributes. A property can have multiple names 
    associated with it, but providers must  ensure that each name is unique.

Use the <b>IADsProperty</b> interface to determine at run time 
    the attribute definition of a property supported by a directory service object.
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To determine the attribute definition at run time</b>
<ol>
<li>Bind to the schema class object of the ADSI object.</li>
<li>Enumerate mandatory or optional attributes accessible from the schema class object. Skip this step if you 
     know that the object supports the attribute of your interest.</li>
<li>Bind to the schema container of the schema class object you obtained in first step.</li>
<li>Retrieve the attribute definition object of the property of interest from the schema container.</li>
<li>Examine the attribute definition of the property. You may have to also inspect the syntax object.</li>
</ol>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsProperty</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> and <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. <b>IADsProperty</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48645dda-ba1e-47fa-b483-120ba982451e">Qualifiers</a>
</td>
<td align="left" width="63%">
Optional additional provider-specific constraints on this property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a>
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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">AdsPath</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Class</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">GUID</a>


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

<a href="https://msdn.microsoft.com/dd348a3c-0386-4fa2-984d-cdea6f09bd72">MaxRange</a>


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

<a href="https://msdn.microsoft.com/dd348a3c-0386-4fa2-984d-cdea6f09bd72">MinRange</a>


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

<a href="https://msdn.microsoft.com/dd348a3c-0386-4fa2-984d-cdea6f09bd72">MultiValued</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Name</a>


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

<a href="https://msdn.microsoft.com/dd348a3c-0386-4fa2-984d-cdea6f09bd72">OID</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Parent</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Schema</a>


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

<a href="https://msdn.microsoft.com/dd348a3c-0386-4fa2-984d-cdea6f09bd72">Syntax</a>


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

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim obj As IADs
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
MsgBox "Attribute: " &amp; pr.Name
MsgBox "Syntax:    " &amp; pr.Syntax
If pr.Multivalued = True Then
    MsgBox "The Owner attribute has multiple values."
Else
    MsgBox "The Owner attribute has a single value."
End If
 
' To further examine the syntax
Set sy = GetObject(sc.AdsPath &amp; "/" &amp; pr.Syntax)
MsgBox "Syntax object: " &amp; sy.Name &amp; " of OleAutoDataType: " _
       &amp; sy.OleAutoDataType

Cleanup:
    If (Err.Number &lt;&gt; 0 ) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If

    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/690b0c96-6319-42d8-8b0e-c43f46f91031">IADsClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

