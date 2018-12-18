---
UID: NF:iads.IADs.GetEx
title: IADs::GetEx
author: windows-sdk-content
description: Retrieves, from the property cache, property values of a given attribute.
old-location: adsi\iads_getex.htm
tech.root: adsi
ms.assetid: cda6b8e7-fadc-4e0b-8217-66b37bf7efbd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEx, GetEx method [ADSI], GetEx method [ADSI],IADs interface, IADs interface [ADSI],GetEx method, IADs.GetEx, IADs::GetEx, _ds_iads_getex, adsi.iads__getex, adsi.iads_getex, iads/IADs::GetEx
ms.topic: method
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
 - IADs.GetEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADs::GetEx


## -description


The <b>IADs::GetEx</b> method retrieves, from the property cache, property values of a given attribute. The returned property values can be single-valued or multi-valued. Unlike the <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a> method, the property values are returned as a variant array of <b>VARIANT</b>, or a variant array of bytes for binary data. A single-valued property is then represented as an array of a single element.


## -parameters




### -param bstrName [in]

Contains a <b>BSTR</b> that specifies the property name.


### -param pvProp [out]

Pointer to a <b>VARIANT</b> that receives the value, or values, of the property.


## -returns



This method supports the standard return values as well as the return values listed in the following list.
      

For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a> and <b>IADs::GetEx</b> methods return a different variant structure for a single-valued property value. If the property is a string, <b>IADs::Get</b> returns a variant of string (VT_BSTR), whereas <b>IADs::GetEx</b> returns a variant array of a <b>VARIANT</b> type string with a single element. Thus, if you are not sure that a multi-valued attribute will return a single value or multiple values, use <b>IADs::GetEx</b>. As it does not require you to validate the result's data structures, you may want to use <b>IADs::GetEx</b> to retrieve a property when you are not sure whether it has single or multiple values. The following list compares the two methods.

<table>
<tr>
<th>IADs::Get version</th>
<th>IADs::GetEx version</th>
</tr>
<tr>
<td>
<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x as IADs

otherNumbers = x.Get("otherHomePhone")
If VarType(otherNumbers) = vbString Then
  Debug.Print otherNumbers
Else
  For Each homeNum In otherNumbers
    Debug.Print homeNum
  Next
End If</pre>
</td>
</tr>
</table></span></div>
</td>
<td>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Dim x as IADs

otherNumbers = x.GetEx("otherHomePhone")
For Each homeNum In otherNumbers
  Debug.Print homeNum
Next</pre>
</td>
</tr>
</table></span></div>
</td>
</tr>
</table>
 

Like the  <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a> method, <b>IADs::GetEx</b> implicitly calls <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a> against an uninitialized property cache. For more information about implicit and explicit calls to <b>IADs::GetInfo</b>, see   <b>IADs::GetInfo</b>.


#### Examples

The following code example shows how to use <b>IADs::GetEx</b> to retrieve object properties.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As IADs
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
</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to retrieve values of the optional properties of an object using the <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a> method.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;HTML&gt;
&lt;head&gt;&lt;title&gt;&lt;/title&gt;&lt;/head&gt;

&lt;body&gt;
&lt;%
Dim x 

On Error Resume Next
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " &amp; x.Name &amp; "&lt;br&gt;"
Response.Write "Object Class: " &amp; x.Class &amp; "&lt;br&gt;"
 
' Get the optional property values for this object.
Set cls = GetObject(x.Schema)
For Each op In cls.OptionalProperties
   vals = obj.GetEx(op)
   if err.Number = 0 then
       Response.Write "Optional Property: &amp; op &amp; "=" 
       for each v in vals 
          Response.Write v &amp; " "
       next
       Response.Write "&lt;br&gt;"
   end if
Next
%&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>
</td>
</tr>
</table></span></div>
The following code example retrieves the "homePhone" property values using <b>IADs::GetEx</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pADs = NULL;
 
hr = ADsGetObject(L"LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=Com", IID_IADs, (void**) &amp;pADs );
if ( !SUCCEEDED(hr) ) { return hr;}
 
hr = pADs-&gt;GetEx(CComBSTR("homePhone"), &amp;var);
if ( SUCCEEDED(hr) )
{
    LONG lstart, lend;
    SAFEARRAY *sa = V_ARRAY( &amp;var );
    VARIANT varItem;
 
    // Get the lower and upper bound.
    hr = SafeArrayGetLBound( sa, 1, &amp;lstart );
    hr = SafeArrayGetUBound( sa, 1, &amp;lend );
 
    // Iterate and print the content.
    VariantInit(&amp;varItem);
    printf("Getting Home Phone using IADs::Get.\n");
    for ( long idx=lstart; idx &lt;= lend; idx++ )
    {
        hr = SafeArrayGetElement( sa, &amp;idx, &amp;varItem );
        printf("%S ", V_BSTR(&amp;varItem));
        VariantClear(&amp;varItem);
    }
    printf("\n");
 
    VariantClear(&amp;var);
}
 
// Cleanup.
if ( pADs )
{
    pADs-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a>



<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a>



<a href="https://msdn.microsoft.com/b3479719-b5bf-4f19-91f9-b05e60bde161">Property Cache Interfaces</a>
 

 

