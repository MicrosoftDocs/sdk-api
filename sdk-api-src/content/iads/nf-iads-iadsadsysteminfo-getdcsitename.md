---
UID: NF:iads.IADsADSystemInfo.GetDCSiteName
title: IADsADSystemInfo::GetDCSiteName
author: windows-sdk-content
description: Retrieves the name of the Active Directory site that contains the local computer.
old-location: adsi\iadsadsysteminfo_getdcsitename.htm
tech.root: ADSI
ms.assetid: 2b9bb5f2-8312-4413-bbf2-4765fd33a2c6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDCSiteName, GetDCSiteName method [ADSI], GetDCSiteName method [ADSI],IADsADSystemInfo interface, IADsADSystemInfo interface [ADSI],GetDCSiteName method, IADsADSystemInfo.GetDCSiteName, IADsADSystemInfo::GetDCSiteName, _ds_iadsadsysteminfo_getdcsitename, adsi.iadsadsysteminfo__getdcsitename, adsi.iadsadsysteminfo_getdcsitename, iads/IADsADSystemInfo::GetDCSiteName
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
 - IADsADSystemInfo.GetDCSiteName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsADSystemInfo::GetDCSiteName


## -description


The <b>IADsADSystemInfo::GetDCSiteName</b> method retrieves the name of the Active Directory site that contains the local computer.


## -parameters




### -param szServer [in]

DNS name of the service server.


### -param pszSiteName

TBD




#### - pbstrSiteName [out]

Name of the Active Directory site.


## -returns



This method supports the standard <b>HRESULT</b> return values. For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



An Active Directory site is one or more well-connected TCP/IP subnets holding Active Directory domain controllers. For more information, see  <a href="https://msdn.microsoft.com/library/Aa772157(v=VS.85).aspx">Active Directory Core Concepts</a>.


#### Examples

The following C++ code example retrieves the Active Directory site name. For brevity, error checking is omitted.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;activeds.h&gt;
#include &lt;stdio.h&gt;
 
int main()
{
    HRESULT hr;
 
    hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&amp;pSys);
 
   BSTR siteName;
   BSTR dnsServer;
   hr = pSys-&gt;GetAnyDCName(&amp;dnsServer);

   if (SUCCEEDED(hr)) {
      printf("Domain controller: %S\n", dnsServer);

      hr = pSys-&gt;GetDCSiteName(&amp;siteName);
      if (SUCCEEDED(hr)) {
          printf("Domain controller site: %S\n", siteName);
          SysFreeString(siteName);
      }

      SysFreeString(dnsServer);
   }

 
   if(pSys) {
      pSys-&gt;Release();
   }
 
   CoUninitialize();
   return 0;
}</pre>
</td>
</tr>
</table></span></div>
The following Visual Basic code example retrieves the name of the Active Directory domain controller site.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim sys As New ADSystemInfo
dc = sys.GetAnyDCName
Debug.Print "Domain Controller site: " &amp; sys.GetDCSiteName(dc)</pre>
</td>
</tr>
</table></span></div>
The following VBScript/ASP code example retrieves the name of the Active Directory domain controller site.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;%
Dim sys

Set sys = CreateObject("ADSystemInfo")

dc = sys.GetAnyDCName

wscript.echo "Domain Controller     : " &amp; dc
wscript.echo "Domain Controller site: " &amp; sys.GetDCSiteName(dc)

%&gt;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="ad.active_directory_core_concepts">Active Directory Core
    Concepts</a>



<a href="https://msdn.microsoft.com/5573d37b-10a8-4176-80c7-711552ff36cb">IADsADSystemInfo</a>
 

 

