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

# SHLoadIndirectString function


## -description


Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).


## -parameters




### -param pszSource [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the indirect string from which the resource will be retrieved. This string should begin with the '@' symbol and use one of the forms discussed in the Remarks section. This function will successfully accept a string that does not begin with an '@' symbol, but the string will be simply passed unchanged to <i>pszOutBuf</i>.


### -param pszOutBuf [out]

Type: <b>PWSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the text resource. Both <i>pszOutBuf</i> and <i>pszSource</i> can point to the same buffer, in which case the original string will be overwritten.


### -param cchOutBuf [in]

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszOutBuf</i>, in characters.


### -param ppvReserved

Type: <b>void**</b>

Not used; set to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An indirect string can be provided in several forms, each of which has its own interpretation:
            
			    

<ul>
<li><b>File name and resource ID</b><pre class="syntax" xml:space="preserve"><code>@filename,resource</code></pre>
The string is extracted from the file named, using the <i>resource</i> value as a locator. If the resource value is zero or greater, the number becomes the index of the string in the binary file. If the number is negative, it becomes a resource ID. The retrieved string is copied to the output buffer and the function returns S_OK.

</li>
<li><b>File name and resource ID with a version modifier</b><pre class="syntax" xml:space="preserve"><code>@filename,resource;v2</code></pre>
This form can be used when a resource is changed but still uses the same index or ID as the old resource. Without a version modifier, the Multilingual User Interface (MUI) cache will not recognize that the resource has changed and will not refresh. By appending the version modifier, the value is seen as a new resource and is added to the cache. Note that it is recommended that you use a new ID or index for a new resource, and use a version modifier only when that is not possible.

</li>
<li><b>PRI file path and resource ID</b><pre class="syntax" xml:space="preserve"><code>@{PRIFilepath?resource}</code></pre>
The Package Resource Index (PRI) is a binary format introduced in Windows 8 that contains indexed resources or references to resources. The .pri file is bundled as part of an app's package. For more information on .pri files, see <a href="4f0d7226-dde6-4241-b4fc-a79a8607ac98">Creating and retrieving resources in Windows Store apps</a>.

The string is extracted from the .pri file named, using the <i>resource</i> as a locator. The retrieved string is copied to the output buffer and the function returns S_OK. The string is extracted based on the current Shell environment or <a href="https://msdn.microsoft.com/bab9ae0f-8609-494d-b943-7905eed8ee93">ResourceContext</a>.

An example of this type of indirect string is shown here:
                        
                            <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
@{C:\Program Files\WindowsApps\Microsoft.Camera_6.2.8376.0_x64__8wekyb3d8bbwe\resources.pri? ms-resource://Microsoft.Camera/resources/manifestAppDescription}</pre>
</td>
</tr>
</table></span></div>


</li>
<li><b>Package name and resource ID</b><pre class="syntax" xml:space="preserve"><code>@{PackageFullName?resource}</code></pre>
The string is extracted from the Resources.pri file stored in the app's root directory of the package identified by <i>PackageFullName</i>, using the <i>resource</i> as a locator. The retrieved string is copied to the output buffer and the function returns S_OK. The string is extracted based on the app's environment or <a href="https://msdn.microsoft.com/bab9ae0f-8609-494d-b943-7905eed8ee93">ResourceContext</a>.

<div class="alert"><b>Note</b>  This string must refer to a package installed for the current user. If it does not, the call will fail.</div>
<div> </div>
An example of this type of indirect string is shown here:
                        
                            <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
@{Microsoft.Camera_6.2.8376.0_x64__8wekyb3d8bbwe? ms-resource://Microsoft.Camera/resources/manifestAppDescription}</pre>
</td>
</tr>
</table></span></div>


</li>
</ul>
If the string is not an indirect string, then the string is directly copied without change to <i>pszOutBuf</i> and the function returns S_OK.



