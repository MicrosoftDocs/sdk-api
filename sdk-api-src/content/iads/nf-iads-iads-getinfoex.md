---
UID: NF:iads.IADs.GetInfoEx
title: IADs::GetInfoEx method
author: windows-driver-content
description: The IADs::GetInfoEx method loads the values of specified properties of the ADSI object from the underlying directory store into the property cache.
old-location: adsi\iads_getinfoex.htm
old-project: ADSI
ms.assetid: 306ab953-890a-4ec9-8ec2-bea73888ea20
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetInfoEx method [ADSI], GetInfoEx method [ADSI], IADs interface, GetInfoEx,IADs.GetInfoEx, IADs, IADs interface [ADSI], GetInfoEx method, IADs::GetInfoEx, _ds_iads_getinfoex, adsi.iads__getinfoex, adsi.iads_getinfoex, iads/IADs::GetInfoEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADs.GetInfoEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADs::GetInfoEx method


## -description


The <b>IADs::GetInfoEx</b> method loads the values of specified properties of the ADSI object from the underlying directory store into the property cache.


## -parameters




### -param vProperties [in]

Array of null-terminated Unicode string entries that list the properties to load into the Active Directory property cache. Each property name must match one in this object's schema class definition.


### -param lnReserved [in]

Reserved for future use. Must be set to zero.


## -returns



This method supports the standard return values, as well as the following.
      

For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The <b>IADs::GetInfoEx</b> method overwrites any previously cached values of the specified properties with those in the directory store. Therefore, any change made to the cache will be lost if <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> was not invoked before the call to <b>IADs::GetInfoEx</b>.

Use <b>IADs::GetInfoEx</b> to refresh values of the selected property in the property cache of an ADSI object. Use <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a> to refresh all the property values.

For an ADSI container object, <b>IADs::GetInfoEx</b> caches only the property values of the container, but not those of the child objects.


#### Examples

The following code example shows how to use the <b>IADs::GetInfoEx</b> to obtain values of the selected properties, assuming that the desired property values can be found in the directory.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As IADs
On Error GoTo Cleanup

Set x = GetObject("LDAP://CN=JeffSmith,CN=Users,DC=Fabrikam,DC=com")
 
' Retrieve givenName and sn from the underlying directory storage.
' Cache should have givenName and sn values.
x.GetInfoEx Array("givenName", "sn"), 0 
Debug.Print x.Get("givenName")  ' Property is in the cache.
Debug.Print x.Get("sn")         ' Property is in the cache.
 
' If the "homePhone" property is not in the cache (in the next line), 
' GetInfo is called implicitly.
Debug.Print x.Get("homePhone")

Cleanup:
   If(Err.Number&lt;&gt;0) Then
      MsgBox("An error has occurred. " &amp; Err.Number);
   End If

   Set x = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to use the <b>IADs::GetInfoEx</b> to obtain values of the selected properties, assuming that the desired property values can be found in the directory. For brevity, error checking has been omitted.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pADs = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
hr = ADsGetObject(L"WinNT://somecomputer,computer",
                  IID_IADs,
                  (void**)&amp;pADs);

if(!(hr==S_OK)){return hr;} 

VariantInit(&amp;var);
 
// Get "Owner" and "Division" attribute values.
LPWSTR pszAttrs[] = { L"Owner", L"Division" };
DWORD dwNumber = sizeof( pszAttrs ) /sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszAttrs, dwNumber, &amp;var );
hr = pADs-&gt;GetInfoEx(var, 0);
VariantClear(&amp;var);
 
hr = pADs-&gt;Get(CComBSTR("Division"), &amp;var);  
printf("    division   = %S\n", V_BSTR(&amp;var));
VariantClear(&amp;var);
hr = pADs-&gt;Get(CComBSTR("Owner"), &amp;var);
printf("    owner      = %S\n", V_BSTR(&amp;var));
VariantClear(&amp;var);

if(pADs)
   pADs-&gt;Release();

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/b3479719-b5bf-4f19-91f9-b05e60bde161">Property
  Cache</a>
 

 

