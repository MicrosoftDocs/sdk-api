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

# IADsPathname::Set


## -description


The <b>IADsPathname::Set</b> method sets up the Pathname object for parsing a directory path. The path is set with a format as defined in  <a href="https://msdn.microsoft.com/fbf7de54-3ea7-4d66-ad56-21cae1e28c07">ADS_SETTYPE_ENUM</a>.


## -parameters




### -param bstrADsPath [in]

Path of an ADSI object.


### -param lnSetType [in]

An <a href="https://msdn.microsoft.com/fbf7de54-3ea7-4d66-ad56-21cae1e28c07">ADS_SETTYPE_ENUM</a> option that defines the format type to be retrieved.


## -returns



This method supports the standard return values, as well as the following:

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



This method will set the namespace as specified and identify the appropriate provider for performing the path cracking operation. Resetting to a different namespace will lose data already set by this method.


#### Examples

The following Visual Basic code example sets a full ADSI path on the Pathname object.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As New Pathname
 
x.Set "LDAP://server/CN=Jeff Smith, DC=Fabrikam, DC=Com", _
       ADS_SETTYPE_FULL
dn = x.GetElement(0)    ' dn now is "CN=Jeff Smith".</pre>
</td>
</tr>
</table></span></div>
The following VBScript/ASP code example sets a full ADSI path on the Pathname object.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;%
Dim x
const ADS_SETTYPE_FULL = 1
Set x = CreateObject("Pathname")
path = "LDAP://server/CN=Jeff Smith, DC=Fabrikam,DC=com" 
x.Set path, ADS_SETTYPE_FULL
dn = x.GetElement(0)    ' dn now is "CN=Jeff Smith".
%&gt;</pre>
</td>
</tr>
</table></span></div>
The following C++ code example sets a full ADSI path on the Pathname object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&amp;pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname-&gt;Release();
    return NULL;
}
 
hr = pPathname-&gt;Set(CComBSTR("LDAP://CN=pencil/desk"), 
                    ADS_SETTYPE_FULL);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/fbf7de54-3ea7-4d66-ad56-21cae1e28c07">ADS_SETTYPE_ENUM</a>



<a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a>
 

 

