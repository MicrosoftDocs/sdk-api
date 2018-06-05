---
UID: NF:iads.IADs.Get
title: IADs::Get
author: windows-sdk-content
description: Retrieves a property of a given name from the property cache.
old-location: adsi\iads_get.htm
old-project: ADSI
ms.assetid: fd6d79b6-46f8-42dd-8525-a72a6e0a7672
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Get, Get method [ADSI], Get method [ADSI],IADs interface, IADs interface [ADSI],Get method, IADs.Get, IADs::Get, _ds_iads_get, adsi.iads__get, adsi.iads_get, iads/IADs::Get
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADs.Get
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADs::Get


## -description


The <b>IADs::Get</b> method retrieves a property of a given name from the property cache. The property can be single-valued, or multi-valued. The property value is represented as either a variant for a single-valued property or a variant array (of <b>VARIANT</b> or bytes) for a property that allows multiple values.


## -parameters




### -param bstrName [in]

Contains a <b>BSTR</b> that specifies the property name.


### -param pvProp [out]

Pointer to a <b>VARIANT</b> that receives the value of the property. For a multi-valued property, <i>pvProp</i> is a variant array of <b>VARIANT</b>, unless the property is a binary type. In this latter case, <i>pvProp</i> is a variant array of bytes (VT_U1 or VT_ARRAY). For the property that refers to an object, <i>pvProp</i> is a VT_DISPATCH pointer to the object referred to.


## -returns



This method supports standard return values, as well as the following.

For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The <b>IADs::Get</b> method requires the caller to handle the single- and multi-valued property values differently. Thus, if you know that the property of interest is either single- or multi-valued, use the <b>IADs::Get</b> method to retrieve the property value. The following code example shows how you, as a caller, can handle single- and multi-valued properties when calling this method.

When a property is uninitialized, calling this method invokes an implicit call to the  <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a> method. This loads from the underlying directory store the values of the supported properties that have not been set in the cache. Any subsequent calls to <b>IADs::Get</b> deals with property values in the cache only. For more information about the behavior of implicit and explicit calls to <b>IADs::GetInfo</b>, see <b>IADs::GetInfo</b>.

You can also use  <a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">IADs::GetEx</a> to retrieve property values from the property cache. However, the values are returned as a variant array of <b>VARIANT</b>s, regardless of whether they are single-valued or multi-valued. That is,  ADSI attempts to package the returned property values in consistent data formats. This saves you, as a caller, the effort of validating the data types when unsure that the returned data has single or multiple values.


#### Examples

The following code example retrieves the security descriptor for an object using <b>IADs::Get</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As IADs
Dim Desc As IADsSecurityDescriptor
On Error GoTo ErrTest:
 
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
 
' Single-valued properties.
Debug.Print "Home Phone Number is: " &amp; x.Get("homePhone")
 
' Some property values represents other ADSI objects. 
' Consult your provider documentation.
Set Desc = x.Get("ntSecurityDescriptor")
 
' Multi-valued property, assuming that multiple values were
' assigned to the "otherHomePhone" properties. Caller must 
' enumerate all the available values.
Debug.Print "Other Phone Numbers are: "
otherNumbers = x.Get("otherHomePhone")
For Each homeNum In otherNumbers
  Debug.Print homeNum
Next
 
Exit Sub
 
ErrTest:
  Debug.Print Hex(Err.Number)
  Set x = Nothing
  Set Desc = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to work with property values of binary data using <b>IADs::Get</b> and  <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim oTarget As IADs
Dim Octet(5) As Byte
Dim MultiOctet(2) As Variant
Dim i As Integer, j As Integer

On Error GoTo Cleanup
 
' Set up MultiOctetString.
For i = 0 To 2
    For j = 0 To 5
        Octet(j) = CByte(i * j)
    Next j
    MultiOctet(i) = Octet
Next i
 
' Bind to the object and set MultiOctetString.
Set oTarget=GetObject("LDAP://CN=SomeUser,CN=Users,DC=Fabrikam, DC=COM")
oTarget.Put "multiOctetString", MultiOctet
oTarget.SetInfo
 
Dim GetOctet As Variant
Dim Temp As Variant
 
' Read back and print MultiOctetString.
GetOctet = oTarget.Get("multiOctetString")
For i = LBound(GetOctet) To UBound(GetOctet)
    Temp = GetOctet(i)
    For j = LBound(Temp) To UBound(Temp)
        Debug.Print Temp(j)
    Next j
    Debug.Print "----"
Next i

Exit Sub

Cleanup:
   MsgBox("An error has occurred. " &amp; Err.Number)
   Set oTarget = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to retrieve values of the optional properties of an object using <b>IADs::Get</b>.

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
 
On error resume next
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " &amp; x.Name &amp; "&lt;br&gt;"
Response.Write "Object Class: " &amp; x.Class &amp; "&lt;br&gt;"
 
' Get optional property values of this object.
Set cls = GetObject(x.Schema)

For Each op In cls.OptionalProperties
   v = obj.Get(op)
   if err.Number = 0 then
       Response.Write "Optional Property: " &amp; op &amp; "=" &amp; v &amp; "&lt;br&gt;"
   end if
Next
%&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>
</td>
</tr>
</table></span></div>
The following code example reads attributes with single and multiple values using <b>IADs::Get</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
IADs *pUsr=NULL;
 
CoInitialize(NULL);
 
///////////////////////////////
// Bind to a directory object.
///////////////////////////////
hr = ADsGetObject(L"WinNT://Fabrikam/Administrator,user", IID_IADs, (void**) &amp;pUsr );
if ( !SUCCEEDED(hr) ) { return hr; }
 
//////////////////////////////////
// Get a single-valued attribute.
//////////////////////////////////
VARIANT var;
VariantInit(&amp;var);
 
hr = pUsr-&gt;Get(CComBSTR("FullName"), &amp;var );
if ( SUCCEEDED(hr) )
{
    printf("FullName: %S\n", V_BSTR(&amp;var) );
    VariantClear(&amp;var);
}
 
if ( pUsr )
{
    pUsr-&gt;Release();
}
 
///////////////////////////////////////////////////////
// Get a multi-valued attribute from a service object.
///////////////////////////////////////////////////////
IADs *pSvc = NULL;
 
hr = ADsGetObject(L"WinNT://Fabrikam/Account/Browser,service", IID_IADs, (void**) &amp;pSvc );
if ( !SUCCEEDED(hr) )
{
    return hr;
}
 
hr = pSvc-&gt;Get(CComBSTR("Dependencies"), &amp;var );
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
    printf("Getting service dependencies using IADs :\n");
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
if ( pSvc )
{
    pSvc-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">IADs::GetEx</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a>



<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a>



<a href="https://msdn.microsoft.com/b3479719-b5bf-4f19-91f9-b05e60bde161">Property
  Cache</a>
 

 

