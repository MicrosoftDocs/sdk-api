---
UID: NF:iads.IADsNameTranslate.InitEx
title: IADsNameTranslate::InitEx (iads.h)
description: Initializes a name translate object by binding to a specified directory server, domain, or global catalog, using the specified user credential.
helpviewer_keywords: ["IADsNameTranslate interface [ADSI]","InitEx method","IADsNameTranslate.InitEx","IADsNameTranslate::InitEx","InitEx","InitEx method [ADSI]","InitEx method [ADSI]","IADsNameTranslate interface","_ds_iadsnametranslate_initex","adsi.iadsnametranslate__initex","adsi.iadsnametranslate_initex","iads/IADsNameTranslate::InitEx"]
old-location: adsi\iadsnametranslate_initex.htm
tech.root: adsi
ms.assetid: 169e1e0d-26c0-484d-b461-8817d37d17b8
ms.date: 12/05/2018
ms.keywords: IADsNameTranslate interface [ADSI],InitEx method, IADsNameTranslate.InitEx, IADsNameTranslate::InitEx, InitEx, InitEx method [ADSI], InitEx method [ADSI],IADsNameTranslate interface, _ds_iadsnametranslate_initex, adsi.iadsnametranslate__initex, adsi.iadsnametranslate_initex, iads/IADsNameTranslate::InitEx
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
 - IADsNameTranslate::InitEx
 - iads/IADsNameTranslate::InitEx
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
 - IADsNameTranslate.InitEx
---

# IADsNameTranslate::InitEx


## -description

The <b>IADsNameTranslate::InitEx</b> method initializes a name translate object by binding to a specified directory server, domain, or global catalog, using the specified user credential. To initialize the object without an explicit user credential, use  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-init">IADsNameTranslate::Init</a>.

The <b>IADsNameTranslate::InitEx</b> method initializes the object by setting the server or domain that the object will point to and supplying a user credential.

## -parameters

### -param lnSetType

A type of initialization to be performed. Possible values are defined in  <a href="/windows/win32/api/iads/ne-iads-ads_name_inittype_enum">ADS_NAME_INITTYPE_ENUM</a>.

### -param bstrADsPath

The name of the server or domain, depending on the value of <i>lnInitType</i>. When <b>ADS_NAME_INITTYPE_GC</b> is issued, this parameter is ignored. The global catalog server of the domain of the current machine will be used to carry out the name translate operations. This method will fail if the computer is not part of a domain, as no global catalog will be found in this scenario. For more information, see <a href="/windows/win32/api/iads/ne-iads-ads_name_inittype_enum">ADS_NAME_INITTYPE_ENUM</a>.

### -param bstrUserID

User name.

### -param bstrDomain

User domain name.

### -param bstrPassword

User password.

## -returns

Returns a standard <b>HRESULT</b> or RPC error code, including:

## -remarks

After the successful initialization, use the name translate object to submit requests of name translations of directory objects. For more information see  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate::Set</a>,  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-get">IADsNameTranslate::Get</a>,  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate::SetEx</a>, or  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-getex">IADsNameTranslate::GetEx</a>.


#### Examples

The following C/C++ code example uses the <b>IADsNameTranslate::InitEx</b> method to initialize an <a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a> object before the distinguished name of a user object is rendered in the s format.


```cpp
IADsNameTranslate *pNto;
HRESULT hr;
hr = CoCreateInstance(CLSID_NameTranslate,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsNameTranslate,
                      (void**)&pNto);
if(FAILED(hr)) { exit 1;}
 
hr = pNto->InitEx(ADS_NAME_INITTYPE_SERVER,
                  CComBSTR("myServer"),
                  CComBSTR("jeffsmith"),
                  CComBSTR("Fabrikam"),
                  CComBSTR("top secret"));
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


The following Visual Basic code example uses the <b>IADsNameTranslate::InitEx</b> method to initialize an <a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a> object in order to have the distinguished name of a user object rendered in the s user name format.


```vb
Dim nto As New NameTranslate
dso="CN=jeffsmith, CN=users, DC=Fabrikam dc=COM"
server = "myServer"
domain = "Fabrikam"
user = "jeffsmith"
passwd = "myPass"
 
nto.InitEx  ADS_NAME_INITTYPE_SERVER, server,user,domain,passwd
nto.Set ADS_NAME_TYPE_1779, dso
trans = nto.Get(ADS_NAME_TYPE_NT4) 
MsgBox "Name in the translated format: " & trans
```


The following VBScript/ASP code example uses the <b>IADsNameTranslate::InitEx</b> method to initialize an <a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a> object in order to have the distinguished name of a user object rendered in the s user name format.


```vb
<%@ Language=VBScript %>
<html>
<body>
<%
  Dim nto
  const ADS_NAME_INITTYPE_SERVER = 2  ' VBScript cannot read 
  const ADS_NAME_TYPE_1779 = 1        ' enumeration definition
  const ADS_NAME_TYPE_NT4 = 3
 
  server = "myServer"
  domain = "Fabrikam"
  user = "jeffsmith"
  passwd = "myPass"
 
  dn = "CN=jeffsmith,CN=Users,DC=Fabrikam,DC=COM" 
 
  Set nto = Server.CreateObject("NameTranslate")
  nto.InitEx ADS_NAME_INITTYPE_SERVER, server,user,domain,passwd
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



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-get">IADsNameTranslate::Get</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-getex">IADsNameTranslate::GetEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate::Set</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate::SetEx</a>