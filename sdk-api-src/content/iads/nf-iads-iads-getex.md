---
UID: NF:iads.IADs.GetEx
title: IADs::GetEx (iads.h)
description: Retrieves, from the property cache, property values of a given attribute.
helpviewer_keywords: ["GetEx","GetEx method [ADSI]","GetEx method [ADSI]","IADs interface","IADs interface [ADSI]","GetEx method","IADs.GetEx","IADs::GetEx","_ds_iads_getex","adsi.iads__getex","adsi.iads_getex","iads/IADs::GetEx"]
old-location: adsi\iads_getex.htm
tech.root: adsi
ms.assetid: cda6b8e7-fadc-4e0b-8217-66b37bf7efbd
ms.date: 12/05/2018
ms.keywords: GetEx, GetEx method [ADSI], GetEx method [ADSI],IADs interface, IADs interface [ADSI],GetEx method, IADs.GetEx, IADs::GetEx, _ds_iads_getex, adsi.iads__getex, adsi.iads_getex, iads/IADs::GetEx
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
 - IADs::GetEx
 - iads/IADs::GetEx
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
 - IADs.GetEx
---

# IADs::GetEx


## -description

The <b>IADs::GetEx</b> method retrieves, from the property cache, property values of a given attribute. The returned property values can be single-valued or multi-valued. Unlike the <a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a> method, the property values are returned as a variant array of <b>VARIANT</b>, or a variant array of bytes for binary data. A single-valued property is then represented as an array of a single element.

## -parameters

### -param bstrName [in]

Contains a <b>BSTR</b> that specifies the property name.

### -param pvProp [out]

Pointer to a <b>VARIANT</b> that receives the value, or values, of the property.

## -returns

This method supports the standard return values as well as the return values listed in the following list.
      

For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The <a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a> and <b>IADs::GetEx</b> methods return a different variant structure for a single-valued property value. If the property is a string, <b>IADs::Get</b> returns a variant of string (VT_BSTR), whereas <b>IADs::GetEx</b> returns a variant array of a <b>VARIANT</b> type string with a single element. Thus, if you are not sure that a multi-valued attribute will return a single value or multiple values, use <b>IADs::GetEx</b>. As it does not require you to validate the result's data structures, you may want to use <b>IADs::GetEx</b> to retrieve a property when you are not sure whether it has single or multiple values. The following list compares the two methods.

<table>
<tr>
<th>IADs::Get version</th>
<th>IADs::GetEx version</th>
</tr>
<tr>
<td>

```vb
Dim x as IADs

otherNumbers = x.Get("otherHomePhone")
If VarType(otherNumbers) = vbString Then
  Debug.Print otherNumbers
Else
  For Each homeNum In otherNumbers
    Debug.Print homeNum
  Next
End If
```


</td>
<td>

```cpp
Dim x as IADs

otherNumbers = x.GetEx("otherHomePhone")
For Each homeNum In otherNumbers
  Debug.Print homeNum
Next
```


</td>
</tr>
</table>
 

Like the  <a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a> method, <b>IADs::GetEx</b> implicitly calls <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> against an uninitialized property cache. For more information about implicit and explicit calls to <b>IADs::GetInfo</b>, see   <b>IADs::GetInfo</b>.


#### Examples

The following code example shows how to use <b>IADs::GetEx</b> to retrieve object properties.


```vb
Dim x As IADs
On Error GoTo ErrTest:
 
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
 
' Single value property.
Debug.Print "Home Phone Number is: " 
phoneNumber = x.GetEx(""homePhone")
For Each homeNum in phoneNumber
    Debug.Print homeNum
Next
 
' Multiple value property.
Debug.Print "Other Phone Numbers are: "
otherNumbers = x.GetEx("otherHomePhone")
For Each homeNum In otherNumbers
    Debug.Print homeNum
Next
Exit Sub
 
ErrTest:
    Debug.Print Hex(Err.Number)
    Set x = Nothing

```


The following code example shows how to retrieve values of the optional properties of an object using the <a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a> method.


```vb
<HTML>
<head><title></title></head>

<body>
<%
Dim x 

On Error Resume Next
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get the optional property values for this object.
Set cls = GetObject(x.Schema)
For Each op In cls.OptionalProperties
   vals = obj.GetEx(op)
   if err.Number = 0 then
       Response.Write "Optional Property: & op & "=" 
       for each v in vals 
          Response.Write v & " "
       next
       Response.Write "<br>"
   end if
Next
%>

</body>
</html>
```


The following code example retrieves the "homePhone" property values using <b>IADs::GetEx</b>.


```cpp
IADs *pADs = NULL;
 
hr = ADsGetObject(L"LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=Com", IID_IADs, (void**) &pADs );
if ( !SUCCEEDED(hr) ) { return hr;}
 
hr = pADs->GetEx(CComBSTR("homePhone"), &var);
if ( SUCCEEDED(hr) )
{
    LONG lstart, lend;
    SAFEARRAY *sa = V_ARRAY( &var );
    VARIANT varItem;
 
    // Get the lower and upper bound.
    hr = SafeArrayGetLBound( sa, 1, &lstart );
    hr = SafeArrayGetUBound( sa, 1, &lend );
 
    // Iterate and print the content.
    VariantInit(&varItem);
    printf("Getting Home Phone using IADs::Get.\n");
    for ( long idx=lstart; idx <= lend; idx++ )
    {
        hr = SafeArrayGetElement( sa, &idx, &varItem );
        printf("%S ", V_BSTR(&varItem));
        VariantClear(&varItem);
    }
    printf("\n");
 
    VariantClear(&var);
}
 
// Cleanup.
if ( pADs )
{
    pADs->Release();
}
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs::PutEx</a>



<a href="/windows/desktop/ADSI/property-cache-interfaces">Property Cache Interfaces</a>