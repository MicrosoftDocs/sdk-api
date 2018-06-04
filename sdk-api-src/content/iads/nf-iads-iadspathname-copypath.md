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

# IADsPathname::CopyPath


## -description


The <b>IADsPathname::CopyPath</b> method 
   creates a copy of the Pathname object.


## -parameters




### -param ppAdsPath [out]

The <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer on the 
      returned <a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a> object.


## -returns



This method supports the standard return values, as well as the following:

For more information and other return values, see <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error 
       Codes</a>.




## -remarks



This method is used to modify the object path and retain the original object path.


#### Examples

The following Visual Basic code example shows how to make a copy of a pathname.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x, y As New Pathname
x.Set "LDAP://srv1/dc=dom,dc=company,dc=com",ADS_SETTYPE_FULL
set y = x.CopyPath
MsgBox y.Retrieve(ADS_FORMAT_WINDOWS)</pre>
</td>
</tr>
</table></span></div>
The following VBScript/ASP code example shows how to make a copy of a pathname.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;%
Dim x, y
Const ADS_SETTYPE_FULL = 1
Const ADS_FORMAT_WINDOWS = 1
Set x = CreateObject("Pathname")
x.Set "LDAP://srv1/dc=dom,dc=company,dc=com",ADS_SETTYPE_FULL
 
set y = x.CopyPath
Response.Write y.Retrieve(ADS_FORMAT_WINDOWS)
%&gt;</pre>
</td>
</tr>
</table></span></div>
The following C++ code example creates a copy of a pathname object. For more information and a code example 
     of the <b>GetPathnameObject</b> function, see 
     <a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsPathname *pPath;
LPWSTR adsPath;
adsPath = L"LDAP://server/cn=jeff smith,dc=Fabrikam,dc=com";
 
IADsPathname *pPath = GetPathnameObject(adsPath)
if (!pPath) exit(0);
 
IDispatch *pDisp;
HRESULT hr;
hr = pPath-&gt;CopyPath(&amp;pDisp);
if(FAILED(hr)) exit(hr);
 
IADsPathname *pPathCopy;
hr = pDisp-&gt;QueryInterface(IID_IADsPathname,(void**)&amp;pPathCopy);
 
// ...</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a>
 

 

