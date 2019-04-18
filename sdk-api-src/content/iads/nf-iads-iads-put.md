---
UID: NF:iads.IADs.Put
title: IADs::Put (iads.h)
author: windows-sdk-content
description: Sets the values of an attribute in the ADSI attribute cache.
old-location: adsi\iads_put.htm
tech.root: adsi
ms.assetid: b543220d-939b-4ca5-9a27-90b04f14be5d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADs interface [ADSI],Put method, IADs.Put, IADs::Put, Put, Put method [ADSI], Put method [ADSI],IADs interface, _ds_iads_put, adsi.iads__put, adsi.iads_put, iads/IADs::Put
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
ms.custom: 19H1
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


```vb
Dim x As IADs
On Error GoTo Cleanup

Set x = GetObject("LDAP://CN=JeffSmith,CN=Users,DC=Fabrikam, DC=Com") 
x.Put "givenName", "Jeff"
x.Put "sn", "Smith"
x.SetInfo    ' Commit to the directory.

Cleanup:
   If(Err.Number<>0) Then
      MsgBox("An error has occurred. " & Err.Number)
   End If
   Set x = Nothing
```


The following code example shows how to use the <b>IADs::Put</b> method.


```cpp
HRESULT hr;
IADs *pADs = NULL;
LPWSTR pszADsPath = L"LDAP://CN=JeffSmith,CN=Users,DC=Fabrikam,DC=com";
 
CoInitialize(NULL);
 
//////////////////////////////////
// Modifying attributes using IADs
//////////////////////////////////
hr = ADsGetObject(pszADsPath, IID_IADs, (void**) &pADs);
 
if(SUCCEEDED(hr))
{ 
    VARIANT var;
    VariantInit(&var);
     
    // Set the first name.
    V_BSTR(&var) = SysAllocString(L"Jeff");
    V_VT(&var) = VT_BSTR;
    hr = pADs->Put(CComBSTR("givenName"), var);
     
    // Set the last name.
    VariantClear(&var);
    V_BSTR(&var) = SysAllocString(L"Smith");
    V_VT(&var) = VT_BSTR;
    hr = pADs->Put(CComBSTR("sn"), var); 
    VariantClear(&var);

    // Other Telephones.
    LPWSTR pszPhones[] = { L"425-707-9790", L"425-707-9791" };
    DWORD dwNumber = sizeof(pszPhones)/sizeof(LPWSTR);
    hr = ADsBuildVarArrayStr(pszPhones, dwNumber, &var);
    hr = pADs->Put(CComBSTR("otherTelephone"), var); 
    VariantClear(&var);
     
    // Commit the change to the directory.
    hr = pADs->SetInfo();
    pADs->Release();
}

CoUninitialize();
```





## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a>



<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">IADs::GetEx</a>



<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a>



<a href="https://msdn.microsoft.com/b3479719-b5bf-4f19-91f9-b05e60bde161">Property
  Cache</a>
 

 

