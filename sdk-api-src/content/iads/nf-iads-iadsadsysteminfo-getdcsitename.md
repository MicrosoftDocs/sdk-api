---
UID: NF:iads.IADsADSystemInfo.GetDCSiteName
title: IADsADSystemInfo::GetDCSiteName (iads.h)
description: Retrieves the name of the Active Directory site that contains the local computer.
helpviewer_keywords: ["GetDCSiteName","GetDCSiteName method [ADSI]","GetDCSiteName method [ADSI]","IADsADSystemInfo interface","IADsADSystemInfo interface [ADSI]","GetDCSiteName method","IADsADSystemInfo.GetDCSiteName","IADsADSystemInfo::GetDCSiteName","_ds_iadsadsysteminfo_getdcsitename","adsi.iadsadsysteminfo__getdcsitename","adsi.iadsadsysteminfo_getdcsitename","iads/IADsADSystemInfo::GetDCSiteName"]
old-location: adsi\iadsadsysteminfo_getdcsitename.htm
tech.root: adsi
ms.assetid: 2b9bb5f2-8312-4413-bbf2-4765fd33a2c6
ms.date: 12/05/2018
ms.keywords: GetDCSiteName, GetDCSiteName method [ADSI], GetDCSiteName method [ADSI],IADsADSystemInfo interface, IADsADSystemInfo interface [ADSI],GetDCSiteName method, IADsADSystemInfo.GetDCSiteName, IADsADSystemInfo::GetDCSiteName, _ds_iadsadsysteminfo_getdcsitename, adsi.iadsadsysteminfo__getdcsitename, adsi.iadsadsysteminfo_getdcsitename, iads/IADsADSystemInfo::GetDCSiteName
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
 - IADsADSystemInfo::GetDCSiteName
 - iads/IADsADSystemInfo::GetDCSiteName
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
 - IADsADSystemInfo.GetDCSiteName
---

# IADsADSystemInfo::GetDCSiteName


## -description

The <b>IADsADSystemInfo::GetDCSiteName</b> method retrieves the name of the Active Directory site that contains the local computer.

## -parameters

### -param szServer [out]

Name of the Active Directory site.

### -param pszSiteName [in]

DNS name of the service server.

## -returns

This method supports the standard <b>HRESULT</b> return values. For more information, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

An Active Directory site is one or more well-connected TCP/IP subnets holding Active Directory domain controllers. For more information, see  <a href="/windows/desktop/AD/core-concepts-of-active-directory-domain-services">Active Directory Core Concepts</a>.


#### Examples

The following C++ code example retrieves the Active Directory site name. For brevity, error checking is omitted.


```cpp
#include <activeds.h>
#include <stdio.h>
 
int main()
{
    HRESULT hr;
 
    hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR siteName;
   BSTR dnsServer;
   hr = pSys->GetAnyDCName(&dnsServer);

   if (SUCCEEDED(hr)) {
      printf("Domain controller: %S\n", dnsServer);

      hr = pSys->GetDCSiteName(&siteName);
      if (SUCCEEDED(hr)) {
          printf("Domain controller site: %S\n", siteName);
          SysFreeString(siteName);
      }

      SysFreeString(dnsServer);
   }

 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```


The following Visual Basic code example retrieves the name of the Active Directory domain controller site.


```vb
Dim sys As New ADSystemInfo
dc = sys.GetAnyDCName
Debug.Print "Domain Controller site: " & sys.GetDCSiteName(dc)
```


The following VBScript/ASP code example retrieves the name of the Active Directory domain controller site.


```vb
<%
Dim sys

Set sys = CreateObject("ADSystemInfo")

dc = sys.GetAnyDCName

wscript.echo "Domain Controller     : " & dc
wscript.echo "Domain Controller site: " & sys.GetDCSiteName(dc)

%>
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/win32/ad/core-concepts-of-active-directory-domain-services">Active Directory Core Concepts</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsadsysteminfo">IADsADSystemInfo</a>