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
    management include <a href="/windows/desktop/api/iads/nn-iads-iadsclass">IADsClass</a> and 
    <a href="/windows/desktop/api/iads/nn-iads-iadssyntax">IADsSyntax</a>.

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

The <b>IADsProperty</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsProperty</b> also has these types of members:

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

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsclass">IADsClass</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
