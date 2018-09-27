---
UID: NN:iads.IADsClass
title: IADsClass
author: windows-sdk-content
description: The IADsClass interface is designed for managing schema class objects that provide class definitions for any ADSI object. Other schema management interfaces include IADsProperty for attribute definitions and IADsSyntax for attribute syntax.
old-location: adsi\iadsclass.htm
tech.root: ADSI
ms.assetid: 690b0c96-6319-42d8-8b0e-c43f46f91031
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsClass, IADsClass interface [ADSI], IADsClass interface [ADSI],described, _ds_iadsclass, adsi.iadsclass, iads/IADsClass
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
 - IADsClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsClass interface


## -description


The <b>IADsClass</b> interface is designed for managing schema class objects that provide class definitions for any ADSI object. Other schema management interfaces include  <a href="https://msdn.microsoft.com/ebf03974-371b-4bf4-91b4-f137339bd784">IADsProperty</a> for attribute definitions and  <a href="https://msdn.microsoft.com/1ff8703f-b89d-435d-81af-e5c9a2dc01e2">IADsSyntax</a> for attribute syntax.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsClass</b> interface inherits from <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. <b>IADsClass</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d05e4278-2dfb-4832-a97d-eb35253ae535">Qualifiers</a>
</td>
<td align="left" width="63%">
Returns a collection of ADSI objects that describe provider-specific qualifiers for the schema.

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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsClass</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">Abstract</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">AuxDerivedFrom</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">Auxiliary</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">CLSID</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">Container</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">Containment</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">DerivedFrom</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">HelpFileContext</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">HelpFileName</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">MandatoryProperties</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">NamingProperties</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">OID</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">OptionalProperties</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">PossibleSuperiors</a>


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

<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">PrimaryInterface</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Schema</a>


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



Schema objects are organized in the schema container of a given directory. To access an object's schema class, use the object's <b>Schema</b> property (namely, call the <a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">IADs::get_Schema</a> property method) to obtain the ADsPath string and use that string to bind to its schema class object.


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




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/ebf03974-371b-4bf4-91b4-f137339bd784">IADsProperty</a>



<a href="https://msdn.microsoft.com/1ff8703f-b89d-435d-81af-e5c9a2dc01e2">IADsSyntax</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

