---
UID: NF:iads.IADsNameTranslate.Init
title: IADsNameTranslate::Init (iads.h)
author: windows-sdk-content
description: Initializes a name translate object by binding to a specified directory server, domain, or global catalog, using the credentials of the current user.
old-location: adsi\iadsnametranslate_init.htm
tech.root: adsi
ms.assetid: dad31301-b18b-44ec-b32f-93d0bb5b6189
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsNameTranslate interface [ADSI],Init method, IADsNameTranslate.Init, IADsNameTranslate::Init, Init, Init method [ADSI], Init method [ADSI],IADsNameTranslate interface, _ds_iadsnametranslate_init, adsi.iadsnametranslate__init, adsi.iadsnametranslate_init, iads/IADsNameTranslate::Init
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
 - IADsNameTranslate.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsNameTranslate::Init


## -description


The <b>IADsNameTranslate::Init</b> method initializes a name translate object by binding to a specified directory server, domain, or global catalog, using the credentials of the current user. To initialize the object with a different user credential, use  <a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">IADsNameTranslate::InitEx</a>.


## -parameters




### -param lnSetType

A type of initialization to be performed. Possible values are defined in  <a href="https://msdn.microsoft.com/cd7e4786-b20c-4dad-bae6-4e703e60f330">ADS_NAME_INITTYPE_ENUM</a>.


### -param bstrADsPath

The name of the server or domain, depending on the value of <i>lnInitType</i>. When <b>ADS_NAME_INITTYPE_GC</b> is issued, this parameter is ignored. The global catalog server of the domain of the current computer will  perform the name translate operations. This method will fail if the computer is not part of a domain as no global catalog will be found in this scenario. For more information, see <a href="https://msdn.microsoft.com/cd7e4786-b20c-4dad-bae6-4e703e60f330">ADS_NAME_INITTYPE_ENUM</a>.


## -returns



Returns a standard <b>HRESULT</b> or RPC error code, including:




## -remarks



After the successful initialization, you can proceed to use the name translate object to submit requests of name translations of objects in the directory. For more information, see  <a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a>, or  <a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate::Get</a>.


#### Examples

The following C/C++ code example uses the <b>IADsNameTranslate::Init</b> method to initialize an <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> object before the distinguished name of a user object is rendered in the s format.


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


The following Visual Basic code example uses the <b>IADsNameTranslate::Init</b> method to initialize an <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> object in order to have the distinguished name of a user object rendered in the s user name format.


```vb
Dim nto As New NameTranslate
dso="CN=jeffsmith, CN=users, DC=Fabrikam dc=COM"
 
nto.Init  ADS_NAME_INITTYPE_SERVER, "myServer"
nto.Set ADS_NAME_TYPE_1779, dso
trans = nto.Get(ADS_NAME_TYPE_NT4)  
```


The following VBScript/ASP code example uses the <b>IADsNameTranslate::Init</b> method to initialize an <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> object in order to have the distinguished name of a user object rendered in the s user name format.


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




<a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>



<a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate::Get</a>



<a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">IADsNameTranslate::InitEx</a>



<a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a>
 

 

