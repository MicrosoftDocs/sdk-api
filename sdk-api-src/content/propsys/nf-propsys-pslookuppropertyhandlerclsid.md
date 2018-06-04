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

# PSLookupPropertyHandlerCLSID function


## -description


Gets the class identifier (CLSID) of a per-computer, registered file property handler.


## -parameters




### -param pszFilePath [in]

Type: <b>PCWSTR</b>

Pointer to a null-terminated, Unicode buffer that contains the absolute path of the file whose property handler CLSID is requested.


### -param pclsid [out]

Type: <b>CLSID*</b>

When this function returns, contains the requested property handler CLSID.


## -returns



Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



For information on how to register your handler, see <a href="shell.Building_Property_Handlers_Property_Handlers">Initializing Property Handlers</a>.

This function returns only those handlers registered under <b>HKEY_LOCAL_MACHINE</b>.

Most calling applications should not need to call this method or use <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create a property handler directly. Instead, calling applications should use <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a> to create a property store for a Shell item on Windows Vista. <b>IShellItem2::GetPropertyStore</b> provides the largest set of available properties for a Shell item, and the most options for customizing exactly which properties to return.

If no property handler is registered for the specified file, this function returns an error code. When this happens, it might still be possible to read certain file system properties from the property store returned from <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a>.

Applications that need to create a property handler from code and that must run both on Windows Vista and on Windows XP can call <a href="shell.PSGetItemPropertyHandler">PSGetItemPropertyHandler</a> to create a property store for a Shell item through the Microsoft Windows Desktop Search (WDS) redistributable.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSLookupPropertyHandlerCLSID">PSLookupPropertyHandlerCLSID</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CLSID clsid;

HRESULT hr = PSLookupPropertyHandlerCLSID(L"C:\\windows\\system32\\shell32.dll", &amp;clsid);

if (SUCCEEDED(hr))
{
    // clsid contains the CLSID of the property handler used for 
    // C:\windows\system32\shell32.dll.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a>



<a href="shell.PSGetItemPropertyHandler">PSGetItemPropertyHandler</a>
 

 

