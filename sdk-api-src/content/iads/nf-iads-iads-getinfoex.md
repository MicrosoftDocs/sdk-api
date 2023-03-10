---
UID: NF:iads.IADs.GetInfoEx
title: IADs::GetInfoEx (iads.h)
description: The IADs::GetInfoEx method loads the values of specified properties of the ADSI object from the underlying directory store into the property cache.
helpviewer_keywords: ["GetInfoEx","GetInfoEx method [ADSI]","GetInfoEx method [ADSI]","IADs interface","IADs interface [ADSI]","GetInfoEx method","IADs.GetInfoEx","IADs::GetInfoEx","_ds_iads_getinfoex","adsi.iads__getinfoex","adsi.iads_getinfoex","iads/IADs::GetInfoEx"]
old-location: adsi\iads_getinfoex.htm
tech.root: adsi
ms.assetid: 306ab953-890a-4ec9-8ec2-bea73888ea20
ms.date: 12/05/2018
ms.keywords: GetInfoEx, GetInfoEx method [ADSI], GetInfoEx method [ADSI],IADs interface, IADs interface [ADSI],GetInfoEx method, IADs.GetInfoEx, IADs::GetInfoEx, _ds_iads_getinfoex, adsi.iads__getinfoex, adsi.iads_getinfoex, iads/IADs::GetInfoEx
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
 - IADs::GetInfoEx
 - iads/IADs::GetInfoEx
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
 - IADs.GetInfoEx
---

# IADs::GetInfoEx


## -description

The <b>IADs::GetInfoEx</b> method loads the values of specified properties of the ADSI object from the underlying directory store into the property cache.

## -parameters

### -param vProperties [in]

Array of null-terminated Unicode string entries that list the properties to load into the Active Directory property cache. Each property name must match one in this object's schema class definition.

### -param lnReserved [in]

Reserved for future use. Must be set to zero.

## -returns

This method supports the standard return values, as well as the following.
      

For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The <b>IADs::GetInfoEx</b> method overwrites any previously cached values of the specified properties with those in the directory store. Therefore, any change made to the cache will be lost if <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> was not invoked before the call to <b>IADs::GetInfoEx</b>.

Use <b>IADs::GetInfoEx</b> to refresh values of the selected property in the property cache of an ADSI object. Use <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> to refresh all the property values.

For an ADSI container object, <b>IADs::GetInfoEx</b> caches only the property values of the container, but not those of the child objects.


#### Examples

The following code example shows how to use the <b>IADs::GetInfoEx</b> to obtain values of the selected properties, assuming that the desired property values can be found in the directory.


```vb
Dim x As IADs
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
   If(Err.Number<>0) Then
      MsgBox("An error has occurred. " & Err.Number);
   End If

   Set x = Nothing

```


The following code example shows how to use the <b>IADs::GetInfoEx</b> to obtain values of the selected properties, assuming that the desired property values can be found in the directory. For brevity, error checking has been omitted.


```cpp
IADs *pADs = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
hr = ADsGetObject(L"WinNT://somecomputer,computer",
                  IID_IADs,
                  (void**)&pADs);

if(!(hr==S_OK)){return hr;} 

VariantInit(&var);
 
// Get "Owner" and "Division" attribute values.
LPWSTR pszAttrs[] = { L"Owner", L"Division" };
DWORD dwNumber = sizeof( pszAttrs ) /sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszAttrs, dwNumber, &var );
hr = pADs->GetInfoEx(var, 0);
VariantClear(&var);
 
hr = pADs->Get(CComBSTR("Division"), &var);  
printf("    division   = %S\n", V_BSTR(&var));
VariantClear(&var);
hr = pADs->Get(CComBSTR("Owner"), &var);
printf("    owner      = %S\n", V_BSTR(&var));
VariantClear(&var);

if(pADs)
   pADs->Release();


```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="/windows/desktop/ADSI/property-cache-interfaces">Property
  Cache</a>