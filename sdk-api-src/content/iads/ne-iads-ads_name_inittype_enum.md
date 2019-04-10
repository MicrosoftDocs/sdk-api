---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0050_0002
title: ADS_NAME_INITTYPE_ENUM (iads.h)
author: windows-sdk-content
description: The ADS_NAME_INITTYPE_ENUM enumeration specifies the types of initialization to perform on a NameTranslate object. It is used in the IADsNameTranslate interface.
old-location: adsi\ads_name_inittype_enum.htm
tech.root: adsi
ms.assetid: cd7e4786-b20c-4dad-bae6-4e703e60f330
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ADS_NAME_INITTYPE_DOMAIN, ADS_NAME_INITTYPE_ENUM, ADS_NAME_INITTYPE_ENUM enumeration [ADSI], ADS_NAME_INITTYPE_GC, ADS_NAME_INITTYPE_SERVER, _ds_ads_name_inittype_enum, adsi.ads__name__inittype__enum, adsi.ads_name_inittype_enum, iads/ADS_NAME_INITTYPE_DOMAIN, iads/ADS_NAME_INITTYPE_ENUM, iads/ADS_NAME_INITTYPE_GC, iads/ADS_NAME_INITTYPE_SERVER
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_NAME_INITTYPE_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_NAME_INITTYPE_ENUM
req.redist: 
---

# ADS_NAME_INITTYPE_ENUM enumeration


## -description


The <b>ADS_NAME_INITTYPE_ENUM</b> enumeration specifies the types of initialization to perform on a <b>NameTranslate</b> object. It is used in the  <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> interface.


## -enum-fields




### -field ADS_NAME_INITTYPE_DOMAIN

Initializes a <b>NameTranslate</b> object by setting the domain that the object binds to.


### -field ADS_NAME_INITTYPE_SERVER

Initializes a <b>NameTranslate</b> object by setting the server that the object binds to.


### -field ADS_NAME_INITTYPE_GC

Initializes a <b>NameTranslate</b> object by locating the global catalog that the object binds to.


## -remarks



The <a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a> method or <a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">IADsNameTranslate::InitEx</a> method uses these options to initialize the <b>NameTranslate</b> object. When <b>ADS_NAME_INITTYPE_SERVER</b> is used, specify the machine name of a directory server. When <b>ADS_NAME_INITTYPE_DOMAIN</b> is set, supply the domain name within a directory forest. When <b>ADS_NAME_INITTYPE_GC</b> is issued, the second parameter in <b>IADsNameTranslate::Init</b> or <b>IADsNameTranslate::InitEx</b> is ignored. The Global Catalog server of the domain of the current computer is used to perform the name translate operations. The initialization fails if the host computer is not part of a domain because no global catalog will be found.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Instead, use the numeric constants to set the appropriate flags in your VBScript applications. To use symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>

#### Examples

The following C/C++ code example uses <a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a> method to initialize a <b>NameTranslate</b> object through the global catalog, assuming the client running the application is within the directory forest. It then renders the distinguished name of a user object in the Windows format.


```cpp
IADsNameTranslate *pNto = NULL;
HRESULT hr = S_OK;
CComBSTR sbstr;

hr = CoCreateInstance(CLSID_NameTranslate,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsNameTranslate,
                      (void**)&pNto);
if(FAILED(hr)) { exit 1;}
 
hr = pNto->Init(ADS_NAME_INITTYPE_GC, CComBSTR(""));
if (FAILED(hr))
{ 
   goto cleanup;
}
 
hr =pNto->Set(ADS_NAME_TYPE_1779,
             CComBSTR(L"cn=jeffsmith,cn=users,dc=Fabrikam,dc=com"));
if(FAILED(hr))
{
   goto cleanup;
}
 
hr = pNto->Get(ADS_NAME_TYPE_NT4, &sbstr);
printf("Name in the translated format: %S\n", sbstr);

cleanup: 
if(pNto)
{
    pNto->Release();
}
```


The following Visual Basic code example  uses the <a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a> method to initialize a <b>NameTranslate</b> object through the global catalog, assuming the client running the application is within the directory forest. It then renders the distinguished name of a user object in the Windows format.


```vb
Dim nto as New NameTranslate
dso="CN=jeffsmith, CN=users, DC=Fabrikam dc=COM"
 
nto.Init  ADS_NAME_INITTYPE_GC, ""
nto.Set ADS_NAME_TYPE_1779, dso
trans = nto.Get(ADS_NAME_TYPE_NT4)   
MsgBox "Translated name = " & trans
```


The following VBScript/ASP code example uses <a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a> method to initialize a <b>NameTranslate</b> object through the global catalog, assuming the client running the application is within the directory forest. It then renders the distinguished name of a user object in the Windows format.


```vb
<%@ Language=VBScript %>
<html>
<body>
<%
  Dim nto
  const ADS_NAME_INITTYPE_GC = 3  ' VBScript cannot read. 
  const ADS_NAME_TYPE_1779 = 1    ' Enumeration definition.
  const ADS_NAME_TYPE_NT4 = 3
 
  dn = "CN=jeff smith,CN=Users,DC=Fabrikam,DC=COM" 
 
  Set nto = Server.CreateObject("NameTranslate")
  nto.Init ADS_NAME_INITTYPE_GC, ""
  nto.Set ADS_NAME_TYPE_1779, dn
  result = nto.Get(ADS_NAME_TYPE_NT4)
 
  Response.Write "<p>Name in the translated format: " & result
 
%>
</body>
</html>
```





## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
  Enumerations</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>
 

 

