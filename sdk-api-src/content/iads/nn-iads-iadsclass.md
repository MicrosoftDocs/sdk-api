---
UID: NN:iads.IADsClass
title: IADsClass (iads.h)
description: The IADsClass interface is designed for managing schema class objects that provide class definitions for any ADSI object. Other schema management interfaces include IADsProperty for attribute definitions and IADsSyntax for attribute syntax.
helpviewer_keywords: ["IADsClass","IADsClass interface [ADSI]","IADsClass interface [ADSI]","described","_ds_iadsclass","adsi.iadsclass","iads/IADsClass"]
old-location: adsi\iadsclass.htm
tech.root: adsi
ms.assetid: 690b0c96-6319-42d8-8b0e-c43f46f91031
ms.date: 12/05/2018
ms.keywords: IADsClass, IADsClass interface [ADSI], IADsClass interface [ADSI],described, _ds_iadsclass, adsi.iadsclass, iads/IADsClass
f1_keywords:
- iads/IADsClass
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
- IADsClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsClass interface


## -description


The <b>IADsClass</b> interface is designed for managing schema class objects that provide class definitions for any ADSI object. Other schema management interfaces include  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsproperty">IADsProperty</a> for attribute definitions and  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssyntax">IADsSyntax</a> for attribute syntax.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsClass</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsClass</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsClass</b> interface has these methods.
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
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsclass-qualifiers">Qualifiers</a>
</td>
<td align="left" width="63%">
Returns a collection of ADSI objects that describe provider-specific qualifiers for the schema.

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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsClass</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">Abstract</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the flag in order to determine whether or not this schema class is abstract.

</td>
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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">AuxDerivedFrom</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the immediate super Auxiliary class of this schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">Auxiliary</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and set the flag in order to determine whether or not this schema class is auxiliary.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">CLSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the CLSID identifying application component that implements this schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">Container</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the flag to indicate whether or not this is a container object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">Containment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets legal objects types that can be contained within this container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">DerivedFrom</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the immediate super class of this schema class.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">HelpFileContext</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the context identifier of an optional help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">HelpFileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the name of an optional help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">MandatoryProperties</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a list of names of the mandatory properties an ADSI object must have.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">NamingProperties</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a list of naming attributes for the schema object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">OID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the directory-specific object identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">OptionalProperties</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a list of names of optional properties an ADSI object may have.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">PossibleSuperiors</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a list of classes that can contain instances of this class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsclass-property-methods">PrimaryInterface</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the identifier of the interface that defines this schema class.

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


## -remarks



Schema objects are organized in the schema container of a given directory. To access an object's schema class, use the object's <b>Schema</b> property (namely, call the <a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">IADs::get_Schema</a> property method) to obtain the ADsPath string and use that string to bind to its schema class object.


#### Examples

The following code example shows how to implement the <b>IADsClass</b> interface.


```vb
Dim obj As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cls = GetObject(obj.Schema)
 
' Inspecting mandatory and optional properties.
For Each p In cls.MandatoryProperties
    MsgBox "Must-have: " & p
Next
For Each p In cls.OptionalProperties
    MsgBox "May-have: " & p
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cls = Nothing
```


The following code example shows how to implement the <b>IADsClass</b> interface.


```cpp
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) { goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) { goto Cleanup; }
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) { goto Cleanup; }
 
VariantInit(&var);
pCls->get_MandatoryProperties(&var);
hr = printVarArray(var);
 
VariantClear(&var);
pCls->get_OptionalProperties(&var);
hr = printVarArray(var);

Cleanup:
    if(pCls)
        pCls->Release();

    if(pADs)
        pADs->Release();

    SysFreeString(bstrSchema);
    VariantClear(&var);
    CoUninitialize();
    return hr;
```


The following code example shows how to implement the <b>printVarArray</b> function.


```cpp
HRESULT printVarArray(VARIANT var)
{
    LONG lstart, lend;
    VARIANT varItem;
    HRESULT hr;
    SAFEARRAY *sa = V_ARRAY( &var );
    hr = SafeArrayGetLBound( sa, 1, &lstart );
    hr = SafeArrayGetUBound( sa, 1, &lend );
    VariantInit(&varItem);
    for ( long idx=lstart; idx <= lend; idx++ ) {
        hr = SafeArrayGetElement( sa, &idx, &varItem );
        printf("   %S \n", V_BSTR(&varItem));
        VariantClear(&varItem);
    }
    printf("\n");
    return S_OK;
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsproperty">IADsProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssyntax">IADsSyntax</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

