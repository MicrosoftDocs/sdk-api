---
UID: NF:winsvc.GetServiceKeyNameA
title: GetServiceKeyNameA function (winsvc.h)
description: Retrieves the service name of the specified service.
helpviewer_keywords: ["GetServiceKeyName","GetServiceKeyName function","GetServiceKeyNameA","GetServiceKeyNameW","_win32_getservicekeyname","base.getservicekeyname","winsvc/GetServiceKeyName","winsvc/GetServiceKeyNameA","winsvc/GetServiceKeyNameW"]
old-location: base\getservicekeyname.htm
tech.root: Services
ms.assetid: d2421566-de4a-49e5-bb41-ea98c6f6d19d
ms.date: 12/05/2018
ms.keywords: GetServiceKeyName, GetServiceKeyName function, GetServiceKeyNameA, GetServiceKeyNameW, _win32_getservicekeyname, base.getservicekeyname, winsvc/GetServiceKeyName, winsvc/GetServiceKeyNameA, winsvc/GetServiceKeyNameW
f1_keywords:
- winsvc/GetServiceKeyName
dev_langs:
- c++
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetServiceKeyNameA function


## -description


Retrieves the service name of the specified service.


## -parameters




### -param hSCManager [in]

A handle to the computer's service control manager database, as returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>.


### -param lpDisplayName [in]

The service display name. This string has a maximum length of 256 characters.


### -param lpServiceName [out, optional]

A pointer to a buffer that receives the service name. If the function fails, this buffer will contain an empty string.

The maximum size of this array is 4K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>lpcchBuffer</i> parameter. The function will fail and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <b>ERROR_INSUFFICIENT_BUFFER</b>. The <i>lpcchBuffer</i> parameter will receive the required size.


### -param lpcchBuffer [in, out]

A pointer to variable that specifies the size of the buffer pointed to by the <i>lpServiceName</i> parameter, in <b>TCHARs</b>. When the function returns, this parameter contains the size of the service name, in <b>TCHARs</b>, excluding the null-terminating character.

If the buffer pointed to by <i>lpServiceName</i> is too small to contain the service name, the function stores no data in it. When the function returns, <i>lpcchBuffer</i> contains the size of the service name, excluding the NULL terminator.


## -returns



If the functions succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



There are two names for a service: the service name and the display name. The service name is the name of the service's key in the registry. The display name is a user-friendly name that appears in the Services control panel application, and is used with the <b>NET START</b> command. Both names are specified with the <a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function and can be modified with the <a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a> function. Information specified for a service is stored in a key with the same name as the service name under the <b>HKEY_LOCAL_MACHINE</b>\<b>System</b>\<b>CurrentControlSet</b>\<b>Services</b>\<i>ServiceName</i> registry key.

To map the service name to the display name, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-getservicedisplaynamea">GetServiceDisplayName</a> function. To map the display name to the service name, use the 
<b>GetServiceKeyName</b> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-getservicedisplaynamea">GetServiceDisplayName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>



<a href="https://docs.microsoft.com/windows/desktop/Services/service-functions">Service Functions</a>
 

 

