---
UID: NF:winsvc.GetServiceKeyNameW
title: GetServiceKeyNameW function
author: windows-sdk-content
description: Retrieves the service name of the specified service.
old-location: base\getservicekeyname.htm
old-project: Services
ms.assetid: d2421566-de4a-49e5-bb41-ea98c6f6d19d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetServiceKeyName, GetServiceKeyName function, GetServiceKeyNameA, GetServiceKeyNameW, _win32_getservicekeyname, base.getservicekeyname, winsvc/GetServiceKeyName, winsvc/GetServiceKeyNameA, winsvc/GetServiceKeyNameW
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
req.unicode-ansi: GetServiceKeyNameW (Unicode) and GetServiceKeyNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - AdvApi32Legacy.dll
 - API-Ms-Win-Service-Core-Ansi-L1-1-0.dll
 - API-MS-Win-Service-Core-Ansi-L1-1-1.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
 - SecHost.dll
api_name:
 - GetServiceKeyName
 - GetServiceKeyNameA
 - GetServiceKeyNameW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetServiceKeyNameW function


## -description


Retrieves the service name of the specified service.


## -parameters




### -param hSCManager [in]

A handle to the computer's service control manager database, as returned by 
<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a>.


### -param lpDisplayName [in]

The service display name. This string has a maximum length of 256 characters.


### -param lpServiceName [out, optional]

A pointer to a buffer that receives the service name. If the function fails, this buffer will contain an empty string.

The maximum size of this array is 4K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>lpcchBuffer</i> parameter. The function will fail and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return <b>ERROR_INSUFFICIENT_BUFFER</b>. The <i>lpcchBuffer</i> parameter will receive the required size.


### -param lpcchBuffer [in, out]

A pointer to variable that specifies the size of the buffer pointed to by the <i>lpServiceName</i> parameter, in <b>TCHARs</b>. When the function returns, this parameter contains the size of the service name, in <b>TCHARs</b>, excluding the null-terminating character.

If the buffer pointed to by <i>lpServiceName</i> is too small to contain the service name, the function stores no data in it. When the function returns, <i>lpcchBuffer</i> contains the size of the service name, excluding the NULL terminator.


## -returns



If the functions succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



There are two names for a service: the service name and the display name. The service name is the name of the service's key in the registry. The display name is a user-friendly name that appears in the Services control panel application, and is used with the <b>NET START</b> command. Both names are specified with the <a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function and can be modified with the <a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a> function. Information specified for a service is stored in a key with the same name as the service name under the <b>HKEY_LOCAL_MACHINE</b>\<b>System</b>\<b>CurrentControlSet</b>\<b>Services</b>\<i>ServiceName</i> registry key.

To map the service name to the display name, use the 
<a href="https://msdn.microsoft.com/704812f3-134c-4161-b3b4-a955d87ff563">GetServiceDisplayName</a> function. To map the display name to the service name, use the 
<b>GetServiceKeyName</b> function.




## -see-also




<a href="https://msdn.microsoft.com/704812f3-134c-4161-b3b4-a955d87ff563">GetServiceDisplayName</a>



<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

