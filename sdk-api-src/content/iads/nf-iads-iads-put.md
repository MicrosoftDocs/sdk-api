---
UID: NF:iads.IADs.Put
title: IADs::Put
author: windows-sdk-content
description: Sets the values of an attribute in the ADSI attribute cache.
old-location: adsi\iads_put.htm
tech.root: ADSI
ms.assetid: b543220d-939b-4ca5-9a27-90b04f14be5d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADs interface [ADSI],Put method, IADs.Put, IADs::Put, Put, Put method [ADSI], Put method [ADSI],IADs interface, _ds_iads_put, adsi.iads__put, adsi.iads_put, iads/IADs::Put
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
 - IADs.Put
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADs::Put


## -description


The <b>IADs::Put</b> method sets the values of an attribute in the ADSI attribute cache.


## -parameters




### -param bstrName [in]

Contains a <b>BSTR</b> that specifies the property name.


### -param vProp [in]

Contains a <b>VARIANT</b> that specifies the new values of the property.


## -returns



This method supports the standard return values, as well as the following.
      

For more information, and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The assignment of the new property values, performed by <b>Put</b> takes place in the property cache only. To propagate the changes to the directory store, call  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> on the object after calling <b>Put</b>.

To manipulate the property values beyond a simple assignment, use  <b>Put</b> to append  or remove a value from an existing array of attribute values.


#### Examples

The following code example shows how to use the <b>IADs::Put</b> method.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As IADs
On Error GoTo Cleanup

Set x = GetObject("LDAP://CN=JeffSmith,CN=Users,DC=Fabrikam, DC=Com") 
x.Put "givenName", "Jeff"
x.Put "sn", "Smith"
x.SetInfo    ' Commit to the directory.

Cleanup:
   If(Err.Number&lt;&gt;0) Then
      MsgBox("An error has occurred. " &amp; Err.Number)
   End If
   Set x = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to use the <b>IADs::Put</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
IADs *pADs = NULL;
LPWSTR pszADsPath = L"LDAP://CN=JeffSmith,CN=Users,DC=Fabrikam,DC=com";
 
CoInitialize(NULL);
 
//////////////////////////////////
// Modifying attributes using IADs
//////////////////////////////////
hr = ADsGetObject(pszADsPath, IID_IADs, (void**) &amp;pADs);
 
if(SUCCEEDED(hr))
{ 
    VARIANT var;
    VariantInit(&amp;var);
     
    // Set the first name.
    V_BSTR(&amp;var) = SysAllocString(L"Jeff");
    V_VT(&amp;var) = VT_BSTR;
    hr = pADs-&gt;Put(CComBSTR("givenName"), var);
     
    // Set the last name.
    VariantClear(&amp;var);
    V_BSTR(&amp;var) = SysAllocString(L"Smith");
    V_VT(&amp;var) = VT_BSTR;
    hr = pADs-&gt;Put(CComBSTR("sn"), var); 
    VariantClear(&amp;var);

    // Other Telephones.
    LPWSTR pszPhones[] = { L"425-707-9790", L"425-707-9791" };
    DWORD dwNumber = sizeof(pszPhones)/sizeof(LPWSTR);
    hr = ADsBuildVarArrayStr(pszPhones, dwNumber, &amp;var);
    hr = pADs-&gt;Put(CComBSTR("otherTelephone"), var); 
    VariantClear(&amp;var);
     
    // Commit the change to the directory.
    hr = pADs-&gt;SetInfo();
    pADs-&gt;Release();
}

CoUninitialize();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a>



<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">IADs::GetEx</a>



<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a>



<a href="https://msdn.microsoft.com/b3479719-b5bf-4f19-91f9-b05e60bde161">Property
  Cache</a>
 

 

