---
UID: NS:mprapi._MPRAPI_ADMIN_DLL_CALLBACKS
title: MPRAPI_ADMIN_DLL_CALLBACKS
author: windows-sdk-content
description: The MPRAPI_ADMIN_DLL_CALLBACKS structure is used by the MprAdminInitializeDllEx function to register the callback function pointers.
old-location: rras\mprapi_admin_dll_callbacks.htm
tech.root: rras
ms.assetid: b36036e3-1aee-41e6-b777-98455b04e44b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMPRAPI_ADMIN_DLL_CALLBACKS, MPRAPI_ADMIN_DLL_CALLBACKS, MPRAPI_ADMIN_DLL_CALLBACKS structure [RAS], MPRAPI_ADMIN_DLL_VERSION_1, MPRAPI_ADMIN_DLL_VERSION_2, PMPRAPI_ADMIN_DLL_CALLBACKS, PMPRAPI_ADMIN_DLL_CALLBACKS structure pointer [RAS], mprapi/MPRAPI_ADMIN_DLL_CALLBACKS, mprapi/PMPRAPI_ADMIN_DLL_CALLBACKS, rras.mprapi_admin_dll_callbacks"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPRAPI_ADMIN_DLL_CALLBACKS
product: Windows
targetos: Windows
req.typenames: MPRAPI_ADMIN_DLL_CALLBACKS, *PMPRAPI_ADMIN_DLL_CALLBACKS
req.redist: 
---

# MPRAPI_ADMIN_DLL_CALLBACKS structure


## -description


The 
<b>MPRAPI_ADMIN_DLL_CALLBACKS</b> structure is used by the 
<a href="https://msdn.microsoft.com/c608c1b3-39de-4c0f-b834-27b9211dffb5">MprAdminInitializeDllEx</a> function to register the  callback function pointers.


## -struct-fields




### -field revision

A value that represents the version of this structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_ADMIN_DLL_VERSION_1"></a><a id="mprapi_admin_dll_version_1"></a><dl>
<dt><b>MPRAPI_ADMIN_DLL_VERSION_1</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure and the callback function pointers that use it as a parameter are not supported by this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_ADMIN_DLL_VERSION_2"></a><a id="mprapi_admin_dll_version_2"></a><dl>
<dt><b>MPRAPI_ADMIN_DLL_VERSION_2</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure and the callback function pointers that use it as a parameter are supported by this structure.

</td>
</tr>
</table>
 


### -field lpfnMprAdminGetIpAddressForUser

A function pointer to an instance of the <a href="https://msdn.microsoft.com/79deeb39-1916-4bb0-b701-8f0a05dc55af">MprAdminGetIpAddressForUser</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef DWORD (APIENTRY * PMPRADMINGETIPADDRESSFORUSER)(WCHAR *, WCHAR *, DWORD *, BOOL *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnMprAdminReleaseIpAddress

A function pointer to an instance of the <a href="https://msdn.microsoft.com/7a1570a9-b43f-4603-a5ed-6d078a5bbb7c">MprAdminReleaseIpAddress</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef VOID  (APIENTRY * PMPRADMINRELEASEIPADRESS)(WCHAR *, WCHAR *, DWORD *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnMprAdminGetIpv6AddressForUser

A function pointer to an instance of the <a href="https://msdn.microsoft.com/ec4b4130-4864-470f-8647-1fcadd359c58">MprAdminGetIpv6AddressForUser</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef DWORD (APIENTRY * PMPRADMINGETIPV6ADDRESSFORUSER)(WCHAR *, WCHAR *, IN6_ADDR *, BOOL *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnMprAdminReleaseIpV6AddressForUser

A function pointer to an instance of the <a href="https://msdn.microsoft.com/c06433b3-d1b0-42d0-993d-5c1cde4cbc0f">MprAdminReleaseIpv6AddressForUser</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef VOID  (APIENTRY * PMPRADMINRELEASEIPV6ADDRESSFORUSER)(WCHAR *, WCHAR *, IN6_ADDR *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnRasAdminAcceptNewLink

A function pointer to an instance of the <a href="https://msdn.microsoft.com/a4cbca7d-a8b0-4396-9201-648bcca6a8c8">MprAdminAcceptNewLink</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef BOOL  (APIENTRY * PMPRADMINACCEPTNEWLINK)(RAS_PORT_0 *, RAS_PORT_1 *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnRasAdminLinkHangupNotification

A function pointer to an instance of the <a href="https://msdn.microsoft.com/7f2b30e8-ba1d-4db3-843f-f9eafca47add">MprAdminLinkHangupNotification</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef VOID  (APIENTRY * PMPRADMINLINKHANGUPNOTIFICATION)(RAS_PORT_0 *, RAS_PORT_1 *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnRasAdminTerminateDll

A function pointer to an instance of the <a href="https://msdn.microsoft.com/7be485ce-fd45-4968-9e9d-2128d5a8967d">MprAdminTerminateDll</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef DWORD (APIENTRY * PMPRADMINTERMINATEDLL)();
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnRasAdminAcceptNewConnectionEx

A function pointer to an instance of the <a href="https://msdn.microsoft.com/398dd922-dd83-402f-b7ad-ce9438f15ca9">MprAdminAcceptNewConnectionEx</a>  callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef BOOL  (APIENTRY * PMPRADMINACCEPTNEWCONNECTIONEX)(RAS_CONNECTION_EX *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnRasAdminAcceptEndpointChangeEx

 


### -field lpfnRasAdminAcceptReauthenticationEx

A function pointer to an instance of the <a href="https://msdn.microsoft.com/32ea0cb5-f67d-4dcc-b5d0-705b6847b163">MprAdminAcceptReauthenticationEx</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef BOOL  (APIENTRY * PMPRADMINACCEPTREAUTHENTICATIONEX)(RAS_CONNECTION_EX *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnRasAdminConnectionHangupNotificationEx

A function pointer to an instance of the <a href="https://msdn.microsoft.com/de251e1b-53ff-45c8-8e2e-65ac26b4a7f5">MprAdminConnectionHangupNotificationEx</a> callback. The callback prototype is defined as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef VOID  (APIENTRY * PMPRADMINCONNECTIONHANGUPNOTIFICATIONEX)(RAS_CONNECTION_EX *);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnRASValidatePreAuthenticatedConnectionEx

 




## -remarks



The following restrictions apply to the callback functions in the <b>MPRAPI_ADMIN_DLL_CALLBACKS</b> structure:

<ul>
<li>Both <b>lpfnMprAdminGetIpv6AddressForUser</b> and <b>lpfnMprAdminReleaseIpV6AddressForUser</b> must be implemented, or neither are implemented.</li>
<li>Both <b>lpfnMprAdminGetIpAddressForUser</b> and <b>lpfnMprAdminReleaseIpAddress</b> must be implemented, or neither are implemented.</li>
<li>Either <b>lpfnRasAdminLinkHangupNotification</b> or <b>lpfnRasAdminAcceptNewLink</b> must be implemented.</li>
<li>Either <b>lpfnRasAdminAcceptNewConnectionEx</b> or <b>lpfnRasAdminConnectionHangupNotificationEx</b> must be implemented.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2029db76-3fe1-4560-b753-910c48cbc578">IN6_ADDR</a>



<a href="https://msdn.microsoft.com/398dd922-dd83-402f-b7ad-ce9438f15ca9">MprAdminAcceptNewConnectionEx</a>



<a href="https://msdn.microsoft.com/a4cbca7d-a8b0-4396-9201-648bcca6a8c8">MprAdminAcceptNewLink</a>



<a href="https://msdn.microsoft.com/32ea0cb5-f67d-4dcc-b5d0-705b6847b163">MprAdminAcceptReauthenticationEx</a>



<a href="https://msdn.microsoft.com/de251e1b-53ff-45c8-8e2e-65ac26b4a7f5">MprAdminConnectionHangupNotificationEx</a>



<a href="https://msdn.microsoft.com/79deeb39-1916-4bb0-b701-8f0a05dc55af">MprAdminGetIpAddressForUser</a>



<a href="https://msdn.microsoft.com/ec4b4130-4864-470f-8647-1fcadd359c58">MprAdminGetIpv6AddressForUser</a>



<a href="https://msdn.microsoft.com/0a53d84e-d9be-4d18-a619-7d92c17b76bb">MprAdminInitializeDll</a>



<a href="https://msdn.microsoft.com/7f2b30e8-ba1d-4db3-843f-f9eafca47add">MprAdminLinkHangupNotification</a>



<a href="https://msdn.microsoft.com/7a1570a9-b43f-4603-a5ed-6d078a5bbb7c">MprAdminReleaseIpAddress</a>



<a href="https://msdn.microsoft.com/c06433b3-d1b0-42d0-993d-5c1cde4cbc0f">MprAdminReleaseIpv6AddressForUser</a>



<a href="https://msdn.microsoft.com/7be485ce-fd45-4968-9e9d-2128d5a8967d">MprAdminTerminateDll</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a>



<a href="https://msdn.microsoft.com/361b065e-8240-465f-a0fe-d4bfc097ec70">RAS_PORT_0</a>



<a href="https://msdn.microsoft.com/4850f08e-13ee-485f-99a5-be4554d6311b">RAS_PORT_1</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

