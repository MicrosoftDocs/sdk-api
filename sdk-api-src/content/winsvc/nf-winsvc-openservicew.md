---
UID: NF:winsvc.OpenServiceW
title: OpenServiceW function
author: windows-sdk-content
description: Opens an existing service.
old-location: base\openservice.htm
old-project: Services
ms.assetid: e0a42613-95ad-4d0f-a464-c6df33014064
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: OpenService, OpenService function, OpenServiceA, OpenServiceW, _win32_openservice, base.openservice, winsvc/OpenService, winsvc/OpenServiceA, winsvc/OpenServiceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenServiceW (Unicode) and OpenServiceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
-	sechost.dll
-	API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
-	API-MS-Win-Service-management-l1-1-0.dll
-	API-MS-Win-Service-Winsvc-l1-1-0.dll
-	API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
-	OpenService
-	OpenServiceA
-	OpenServiceW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OpenServiceW function


## -description


Opens an existing service.


## -parameters




### -param hSCManager [in]

A handle to the service control manager database. The 
<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a> function returns this handle. For more information, see <a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


### -param lpServiceName [in]

The name of the service to be opened. This is the name specified by the <i>lpServiceName</i> parameter of the <a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function when the service object was created, not the service display name that is shown by user interface applications to identify the service. 

The maximum string length is 256 characters. The service control manager database preserves the case of the characters, but service name comparisons are always case insensitive. Forward-slash (/) and backslash (\) are invalid service name characters.


### -param dwDesiredAccess [in]

The access to the service. For a list of access rights, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>. 




Before granting the requested access, the system checks the access token of the calling process against the discretionary access-control list of the security descriptor associated with the service object.


## -returns



If the function succeeds, the return value is a handle to the service.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Others can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The handle does not have access to the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The specified service name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified service does not exist.

</td>
</tr>
</table>
 




## -remarks



The returned handle is only valid for the process that called 
<b>OpenService</b>. It can be closed by calling the 
<a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a> function.

To use <b>OpenService</b>, no privileges are required aside from <b>SC_MANAGER_CONNECT</b>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7ee5254d-b035-4888-88e9-93e3e55d737e">Starting a Service</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>



<a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a>



<a href="https://msdn.microsoft.com/c112b587-7455-4f15-93e1-ded73de6dbbd">ControlService</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/5b0fc714-60e0-4ae3-8fa8-ace36dab2fb0">DeleteService</a>



<a href="https://msdn.microsoft.com/905d4453-96d4-4055-8a17-36714c547cdd">EnumDependentServices</a>



<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a>



<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a>



<a href="https://msdn.microsoft.com/499b63fd-e77b-4b90-9ee7-ff4b7b12c431">QueryServiceDynamicInformation</a>



<a href="https://msdn.microsoft.com/5d95945f-f11b-42af-b302-8d924917b9ab">QueryServiceObjectSecurity</a>



<a href="https://msdn.microsoft.com/3fe02245-97b1-49f3-8f35-2dcd6f221547">QueryServiceStatusEx</a>



<a href="https://msdn.microsoft.com/5ffdd1a9-1a66-4fc4-b35d-4f744bae4897">SCM Handles</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/39481d9a-79d5-4bbf-8480-4095a34dddb6">SetServiceObjectSecurity</a>



<a href="https://msdn.microsoft.com/f185a878-e1c3-4fe5-8ec9-c5296d27f985">StartService</a>
 

 

