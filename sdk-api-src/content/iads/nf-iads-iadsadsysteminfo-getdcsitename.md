---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IADsADSystemInfo::GetDCSiteName


## -description


The <b>IADsADSystemInfo::GetDCSiteName</b> method retrieves the name of the Active Directory site that contains the local computer.


## -parameters




### -param szServer [in]

DNS name of the service server.


### -param pszSiteName






#### - pbstrSiteName [out]

Name of the Active Directory site.


## -returns



This method supports the standard <b>HRESULT</b> return values. For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



An Active Directory site is one or more well-connected TCP/IP subnets holding Active Directory domain controllers. For more information, see  <a href="ad.active_directory_core_concepts">Active Directory Core Concepts</a>.


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
 

 

