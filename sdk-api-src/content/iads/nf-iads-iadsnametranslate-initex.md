---
UID: NF:iads.IADsNameTranslate.InitEx
title: IADsNameTranslate::InitEx
author: windows-sdk-content
description: Initializes a name translate object by binding to a specified directory server, domain, or global catalog, using the specified user credential.
old-location: adsi\iadsnametranslate_initex.htm
tech.root: adsi
ms.assetid: 169e1e0d-26c0-484d-b461-8817d37d17b8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IADsNameTranslate interface [ADSI],InitEx method, IADsNameTranslate.InitEx, IADsNameTranslate::InitEx, InitEx, InitEx method [ADSI], InitEx method [ADSI],IADsNameTranslate interface, _ds_iadsnametranslate_initex, adsi.iadsnametranslate__initex, adsi.iadsnametranslate_initex, iads/IADsNameTranslate::InitEx
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
 - IADsNameTranslate.InitEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsNameTranslate::InitEx


## -description


The <b>IADsNameTranslate::InitEx</b> method initializes a name translate object by binding to a specified directory server, domain, or global catalog, using the specified user credential. To initialize the object without an explicit user credential, use  <a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a>.

The <b>IADsNameTranslate::InitEx</b> method initializes the object by setting the server or domain that the object will point to and supplying a user credential.


## -parameters




### -param lnSetType

A type of initialization to be performed. Possible values are defined in  <a href="https://msdn.microsoft.com/cd7e4786-b20c-4dad-bae6-4e703e60f330">ADS_NAME_INITTYPE_ENUM</a>.


### -param bstrADsPath

The name of the server or domain, depending on the value of <i>lnInitType</i>. When <b>ADS_NAME_INITTYPE_GC</b> is issued, this parameter is ignored. The global catalog server of the domain of the current machine will be used to carry out the name translate operations. This method will fail if the computer is not part of a domain, as no global catalog will be found in this scenario. For more information, see <a href="https://msdn.microsoft.com/cd7e4786-b20c-4dad-bae6-4e703e60f330">ADS_NAME_INITTYPE_ENUM</a>.


### -param bstrUserID

User name.


### -param bstrDomain

User domain name.


### -param bstrPassword

User password.


## -returns



Returns a standard <b>HRESULT</b> or RPC error code, including:




## -remarks



After the successful initialization, use the name translate object to submit requests of name translations of directory objects. For more information see  <a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a>,  <a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate::Get</a>,  <a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate::SetEx</a>, or  <a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate::GetEx</a>.


#### Examples

The following C/C++ code example uses the <b>IADsNameTranslate::InitEx</b> method to initialize an <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> object before the distinguished name of a user object is rendered in the s format.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsNameTranslate *pNto;
HRESULT hr;
hr = CoCreateInstance(CLSID_NameTranslate,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsNameTranslate,
                      (void**)&amp;pNto);
if(FAILED(hr)) { exit 1;}
 
hr = pNto-&gt;InitEx(ADS_NAME_INITTYPE_SERVER,
                  CComBSTR("myServer"),
                  CComBSTR("jeffsmith"),
                  CComBSTR("Fabrikam"),
                  CComBSTR("top secret"));
if (FAILED(hr)) { exit 1;}
 
hr =pNto-&gt;Set(ADS_NAME_TYPE_1779,
             CComBSTR("cn=jeffsmith,cn=users,dc=Fabrikam,dc=com"));
if(FAILED(hr)) {exit 1;}
 
BSTR bstr;
hr = pNto-&gt;Get(ADS_NAME_TYPE_NT4, &amp;bstr);
printf("Name in the translated format: %S\n", bstr);
 
SysFreeString(bstr);
pNto-&gt;Release();</pre>
</td>
</tr>
</table></span></div>
The following Visual Basic code example uses the <b>IADsNameTranslate::InitEx</b> method to initialize an <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> object in order to have the distinguished name of a user object rendered in the s user name format.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim nto As New NameTranslate
dso="CN=jeffsmith, CN=users, DC=Fabrikam dc=COM"
server = "myServer"
domain = "Fabrikam"
user = "jeffsmith"
passwd = "myPass"
 
nto.InitEx  ADS_NAME_INITTYPE_SERVER, server,user,domain,passwd
nto.Set ADS_NAME_TYPE_1779, dso
trans = nto.Get(ADS_NAME_TYPE_NT4) 
MsgBox "Name in the translated format: " &amp; trans</pre>
</td>
</tr>
</table></span></div>
The following VBScript/ASP code example uses the <b>IADsNameTranslate::InitEx</b> method to initialize an <a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a> object in order to have the distinguished name of a user object rendered in the s user name format.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;body&gt;
&lt;%
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
 
  Response.Write "&lt;p&gt;Name in the translated format: " &amp; result
 
%&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>



<a href="https://msdn.microsoft.com/6c8246a9-657e-4db1-ae8f-d9c0a2d41397">IADsNameTranslate::Get</a>



<a href="https://msdn.microsoft.com/01c4fc79-ed5b-4a24-9b97-25b4095a9c8f">IADsNameTranslate::GetEx</a>



<a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a>



<a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate::SetEx</a>
 

 

