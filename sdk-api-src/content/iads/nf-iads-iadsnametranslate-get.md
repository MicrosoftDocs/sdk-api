---
UID: NF:iads.IADsNameTranslate.Get
title: IADsNameTranslate::Get (iads.h)
author: windows-sdk-content
description: Retrieves the name of a directory object in the specified format.
old-location: adsi\iadsnametranslate_get.htm
tech.root: adsi
ms.assetid: 6c8246a9-657e-4db1-ae8f-d9c0a2d41397
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Get, Get method [ADSI], Get method [ADSI],IADsNameTranslate interface, IADsNameTranslate interface [ADSI],Get method, IADsNameTranslate.Get, IADsNameTranslate::Get, _ds_iadsnametranslate_get, adsi.iadsnametranslate__get, adsi.iadsnametranslate_get, iads/IADsNameTranslate::Get
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
 - IADsNameTranslate.Get
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsNameTranslate::Get


## -description


The <b>IADsNameTranslate::Get</b> method retrieves the name of a directory object in the specified format. The distinguished name must have been set in the appropriate format by the  <a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a> method.


## -parameters




### -param lnFormatType

The format type of the output name. For more information, see  <a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>. This method does not support the <b>ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME</b> element in <b>ADS_NAME_TYPE_ENUM</b>.


### -param pbstrADsPath

The name of the returned object.


## -returns



This method supports the standard <b>HRESULT</b> return values, including:




## -remarks



This method lets you retrieve the name of a single directory object. To retrieve names of multiple objects use  <a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate::GetEx</a>.

When referral chasing is on, this method will attempt to chase and resolve the path of a specified object that is not residing on the connected server.


#### Examples

The following C/C++ code example shows how to translate a distinguished name that is compliant with RFC 1779 to a GUID format. The computer name of the directory server is "myServer".


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
 
hr =pNto->Set(ADS_NAME_TYPE_1779, CComBSTR
  ("CN=jeff,CN=Users,DC=myDomain,DC=Fabrikam,DC=COM,O=Internet"));
if(FAILED(hr)) {exit 1;}
 
BSTR bstr;
hr = pNto->Get(ADS_NAME_TYPE_GUID, &bstr);
printf("Translation: %S\n", bstr);
 
SysFreeString(bstr);
pNto->Release();
```


The following Visual Basic code example shows how to translate a distinguished name that is compliant RFC 1779 to a GUID format. The computer name of the directory server is "myServer".


```vb
Dim nto As New NameTranslate
Dim result As String
 
dn = "CN=rob,CN=Users,DC=myDomain,DC=Fabrikam,DC=COM,O=Internet" 
nto.Init ADS_NAME_INITTYPE_SERVER, "myServer"
nto.Set ADS_NAME_TYPE_1779, dn
result = nto.Get ADS_NAME_TYPE_GUID
MsgBox result
```


The following VBScript/ASP code example shows how to translate a distinguished name that is compliant with RFC 1779 to a GUID format. The machine name of the directory server is "myServer".


```vb
<%@ Language=VBScript %>
<html>
<body>
<%
  Dim nto
  const ADS_NAME_INITTYPE_SERVER = 2
  const ADS_NAME_TYPE_1779 = 1
  const ADS_NAME_TYPE_NT4 = 3
 
  server = "myServer"
  user   = "jeffsmith"
  dom    = "Fabrikam"
  passwd = "top secret" 
 
  Set nto = Server.CreateObject("NameTranslate")
  nto.InitEx ADS_NAME_INITTYPE_SERVER, server, user, dom, passwd
  nto.Set ADS_NAME_TYPE_1779, dn
  result = nto.Get(ADS_NAME_TYPE_GUID)
 
  Response.Write "<p>Translated name: " & result
 
%>
</body>
</html>
```





## -see-also




<a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>



<a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate::GetEx</a>



<a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a>
 

 

