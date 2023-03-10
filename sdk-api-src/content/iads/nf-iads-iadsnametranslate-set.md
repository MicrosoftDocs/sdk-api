---
UID: NF:iads.IADsNameTranslate.Set
title: IADsNameTranslate::Set (iads.h)
description: Directs the directory service to set up a specified object for name translation.
helpviewer_keywords: ["IADsNameTranslate interface [ADSI]","Set method","IADsNameTranslate.Set","IADsNameTranslate::Set","Set","Set method [ADSI]","Set method [ADSI]","IADsNameTranslate interface","_ds_iadsnametranslate_set","adsi.iadsnametranslate__set","adsi.iadsnametranslate_set","iads/IADsNameTranslate::Set"]
old-location: adsi\iadsnametranslate_set.htm
tech.root: adsi
ms.assetid: 1c126333-3d5c-4ba3-8c66-de778e26488f
ms.date: 12/05/2018
ms.keywords: IADsNameTranslate interface [ADSI],Set method, IADsNameTranslate.Set, IADsNameTranslate::Set, Set, Set method [ADSI], Set method [ADSI],IADsNameTranslate interface, _ds_iadsnametranslate_set, adsi.iadsnametranslate__set, adsi.iadsnametranslate_set, iads/IADsNameTranslate::Set
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
 - IADsNameTranslate::Set
 - iads/IADsNameTranslate::Set
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
 - IADsNameTranslate.Set
---

# IADsNameTranslate::Set


## -description

The <b>IADsNameTranslate::Set</b> method directs the directory service to set up a specified object for name translation. To set the names and format of multiple objects, use  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsnametranslate::SetEx</a>.

## -parameters

### -param lnSetType

The format of the name of a directory object. For more information, see  <a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>.

### -param bstrADsPath

The object name, for example, "CN=Administrator, CN=users, DC=Fabrikam, DC=com".

## -returns

This method supports the standard <b>HRESULT</b> return values, including:

## -remarks

Before calling this method to set the object name, you should have established a connection to the directory service using either  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-init">IADsNameTranslate::Init</a> or  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-initex">IADsNameTranslate::InitEx</a>.

You can use the <b>IADsNameTranslate::Set</b> method to set name translation for objects residing on the directory server. When the referral chasing is on, this method will also set any object found on other servers. For more information about referral chasing, see  <a href="/windows/desktop/ADSI/iadsnametranslate-property-methods">IADsNameTranslate Property Methods</a>.


#### Examples

The following C/C++ code example uses the <b>IADsNameTranslate::Set</b> method to set an object so that its name can be translated from the RFC 1779 format to the s user name format.


```cpp
IADsNameTranslate *pNto;
HRESULT hr;
hr = CoCreateInstance(CLSID_NameTranslate,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsNameTranslate,
                      (void**)&pNto);
if(FAILED(hr)) { exit 1;}
 
hr = pNto->Init(ADS_NAME_INITTYPE_SERVER,
                  CComBSTR("myServer"));
if (FAILED(hr)) { exit 1;}
 
hr =pNto->Set(ADS_NAME_TYPE_1779,
             CComBSTR("cn=jeffsmith,cn=users,dc=Fabrikam,dc=com"));
if(FAILED(hr)) {exit 1;}
 
BSTR bstr;
hr = pNto->Get(ADS_NAME_TYPE_NT4, &bstr);
printf("Name in the translated format: %S\n", bstr);
 
SysFreeString(bstr);
pNto->Release();
```


The following Visual Basic code example uses the <b>IADsNameTranslate::Set</b> method to set an object so that its name can be translated from the RFC 1779 format to the s user name format.


```vb
Dim nto As New NameTranslate
dso="CN=jeffsmith, CN=users, DC=Fabrikam dc=COM"
 
nto.Init ADS_NAME_INITTYPE_SERVER, "myServer"
nto.Set ADS_NAME_TYPE_1779, dso
trans = nto.Get(ADS_NAME_TYPE_NT4)  
```


The following VBScript/ASP code example uses the <b>IADsNameTranslate::Set</b> method to set an object to have its name translated from the RFC 1779 format to the s user name format.


```vb
<%@ Language=VBScript %>
<html>
<body>
<%
  Dim nto
  const ADS_NAME_INITTYPE_SERVER = 2  ' VBScript cannot read 
  const ADS_NAME_TYPE_1779 = 1        ' enumeration definition
  const ADS_NAME_TYPE_NT4 = 3
 
  dn = "CN=jeffsmith,CN=Users,DC=Fabrikam,DC=COM" 
 
  Set nto = Server.CreateObject("NameTranslate")
  nto.Init ADS_NAME_INITTYPE_SERVER, "myServer"
  nto.Set ADS_NAME_TYPE_1779, dn
  result = nto.Get(ADS_NAME_TYPE_NT4)
 
  Response.Write "<p>Name in the translated format: " & result
 
%>
</body>
</html>
```

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a>



<a href="/windows/desktop/ADSI/iadsnametranslate-property-methods">IADsNameTranslate Property Methods</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-init">IADsNameTranslate::Init</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-initex">IADsNameTranslate::InitEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate::SetEx</a>