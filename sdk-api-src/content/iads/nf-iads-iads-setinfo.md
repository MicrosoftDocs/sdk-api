---
UID: NF:iads.IADs.SetInfo
title: IADs::SetInfo (iads.h)
description: The IADs::SetInfo method saves the cached property values of the ADSI object to the underlying directory store.
helpviewer_keywords: ["IADs interface [ADSI]","SetInfo method","IADs.SetInfo","IADs::SetInfo","SetInfo","SetInfo method [ADSI]","SetInfo method [ADSI]","IADs interface","_ds_iads_setinfo","adsi.iads__setinfo","adsi.iads_setinfo","iads/IADs::SetInfo"]
old-location: adsi\iads_setinfo.htm
tech.root: adsi
ms.assetid: e7ff6acd-b7c4-463d-a34f-fd793067c63a
ms.date: 12/05/2018
ms.keywords: IADs interface [ADSI],SetInfo method, IADs.SetInfo, IADs::SetInfo, SetInfo, SetInfo method [ADSI], SetInfo method [ADSI],IADs interface, _ds_iads_setinfo, adsi.iads__setinfo, adsi.iads_setinfo, iads/IADs::SetInfo
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
 - IADs::SetInfo
 - iads/IADs::SetInfo
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
 - IADs.SetInfo
---

# IADs::SetInfo


## -description

The <b>IADs::SetInfo</b> method saves the cached property values of the ADSI object to the underlying directory store.



## -returns

This method supports the standard return values, including S_OK for a successful operation. For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

It is important to emphasize the differences between the  <a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a> and <b>IADs::SetInfo</b> methods. The former sets (or modifies) values of a given property in the property cache whereas the latter propagates the changes from the property cache into the underlying directory store. Therefore, any property value changes made by <b>IADs::Put</b> will be lost if <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> (or <a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>) is invoked before <b>IADs::SetInfo</b> is called.

Because <b>IADs::SetInfo</b> sends data across networks, minimize the usage of this method. This reduces the number of trips  a client makes to the server. For example, you should commit all, or most, of the changes to the properties from the cache to the persistent store in one batch.

This guideline pertains only to the relationship of <b>IADs::SetInfo</b> with the <a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a> method, which differs from the relationship with the <a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs::PutEx</a> method.

The following code example illustrates the recommended  relation between <a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a> and <b>IADs::SetInfo</b>.


```vb
Dim obj as IADs
 
obj.Put(prop1,val1)
obj.Put(prop2.val2)
obj.Put(prop3.val3)
obj.SetInfo
```


The following code example illustrates what is not recommended between <a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a> and <b>IADs::SetInfo</b>.


```vb
obj.Put(prop1,val1)
obj.SetInfo
obj.Put(prop2.val2)
obj.SetInfo
obj.Put(prop3.val3)
obj.SetInfo
```


When used with  <a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs::PutEx</a>, <b>IADs::SetInfo</b> passes the operational requests specified by control codes, such as ADS_PROPERTY_UPDATE or ADS_PROPERTY_CLEAR, to the underlying directory store.


#### Examples

The following Visual Basic code example uses the <b>IADs::SetInfo</b> method to save the property value of a user to the underlying directory.


```vb
Dim x as IADs
On Error GoTo Cleanup

Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'
' Update values in the cache.
'
x.Put "sn", "Smith"
x.Put "givenName", "Jeff"
x.Put "street", "1 Tanka Place"
x.Put "l", "Sammamish"
x.Put "st", "Washington"
'
' Commit changes to the directory.
x.SetInfo

Cleanup:
   If (Err.Number<>0) Then
      MsgBox("An error has occurred. " & Err.Number)
   End If
   Set x = Nothing

```


The following C++ code example updates property values in the property cache and commits the change to the directory store using <b>IADs::SetInfo</b>. For brevity, error checking is omitted.


```cpp
IADs *pAds NULL;
VARIANT var;
HRESULT hr = S_OK;
LPWSTR path=L"LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com";
hr = ADsGetObject( path, IID_IADs, (void**) pADs);

if(!(hr==S_OK)) {return hr;}

VariantInit(&var);
// Update values in the cache.
V_BSTR(&var) = SysAllocString(L"Smith");
V_VT(&var) = VT_BSTR;
hr = pADs->Put(CComBSTR("sn"), var );
VariantClear(&var);
 
V_BSTR(&var) = SysAllocString(L"Jeff");
V_VT(&var) = VT_BSTR;
hr = pADs->Put(CComBSTR("givenName"), var );
VariantClear(&var);
 
V_BSTR(&var) = SysAllocString(L"1 Tanka Place");
V_VT(&var) = VT_BSTR;
hr = pADs->Put(CComBSTR("street"), var );
VariantClear(&var);
 
V_BSTR(&var) = SysAllocString(L"Sammamish");
V_VT(&var) = VT_BSTR;
hr = pADs->Put(CComBSTR("l"), var );
VariantClear(&var);
 
V_BSTR(&var) = SysAllocString(L"Washington");
V_VT(&var) = VT_BSTR;
hr = pADs->Put(CComBSTR("st"), var );
VariantClear(&var);
 
// Commit changes to the directory store.
hr = pADs->SetInfo();

if(pADs)
   pADs->Release();
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs::PutEx</a>
