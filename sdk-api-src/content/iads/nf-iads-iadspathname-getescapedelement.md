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

# IADsPathname::GetEscapedElement


## -description


The <b>IADsPathname::GetEscapedElement</b> method is used to escape special characters in the input path.


## -parameters




### -param lnReserved [in]

Reserved for future use.


### -param bstrInStr [in]

An input string.


### -param pbstrOutStr






#### - bstrOutStr [out]

An output string.


## -returns



This method supports the standard return values, as well as the following:

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



This method is used to handle a path that contains special characters in a unescaped string as input from a user interface. The input string must be a single element (name-value pair) of the path; that is, "CN=Smith,Jeff".


#### Examples

The following Visual Basic code example shows the effect produced by <b>IADsPathname::GetEscapedElement</b>. After this code is executed, rdn will contain "cn=smith\,jeff".

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As New Pathname
 
rdn = x.GetEscapedElement(0, "cn=smith,jeff")</pre>
</td>
</tr>
</table></span></div>
The following VBScript code example shows the effect produced by <b>IADsPathname::GetEscapedElement</b>. After this code is executed, rdn will contain "cn=smith\,jeff".

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x 
Set x = CreateObject("Pathname")
rdn = x.GetEscapedElement(0, "cn=smith,jeff")</pre>
</td>
</tr>
</table></span></div>
The following C++ code example shows the effect produced by <b>IADsPathname::GetEscapedElement</b>. After this code is executed, rdn will contain "cn=smith\,jeff".

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPWSTR adsPath=L"LDAP://server/cn=jeffsmith,dc=Fabrikam,dc=com";
 
IADsPathname *pPath = GetPathnameObject(adsPath);
BSTR rdn;
HRESULT hr = pPath-&gt;GetEscapedElement(0,CComBSTR("cn=smith,jeff")
                                      ,&amp;rdn);
 
pPath-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a>
 

 

