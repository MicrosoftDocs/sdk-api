---
UID: NF:winsvc.GetServiceDisplayNameW
title: GetServiceDisplayNameW function (winsvc.h)
description: Retrieves the display name of the specified service. (Unicode)
helpviewer_keywords: ["GetServiceDisplayName", "GetServiceDisplayName function", "GetServiceDisplayNameW", "_win32_getservicedisplayname", "base.getservicedisplayname", "winsvc/GetServiceDisplayName", "winsvc/GetServiceDisplayNameW"]
old-location: base\getservicedisplayname.htm
tech.root: security
ms.assetid: 704812f3-134c-4161-b3b4-a955d87ff563
ms.date: 12/05/2018
ms.keywords: GetServiceDisplayName, GetServiceDisplayName function, GetServiceDisplayNameA, GetServiceDisplayNameW, _win32_getservicedisplayname, base.getservicedisplayname, winsvc/GetServiceDisplayName, winsvc/GetServiceDisplayNameA, winsvc/GetServiceDisplayNameW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetServiceDisplayNameW (Unicode) and GetServiceDisplayNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetServiceDisplayNameW
 - winsvc/GetServiceDisplayNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-service-core-l1-1-5.dll
 - api-ms-win-service-core-l1-1-4.dll
 - api-ms-win-service-core-l1-1-3.dll
 - Advapi32.dll
 - AdvApi32Legacy.dll
 - API-Ms-Win-Service-Core-Ansi-L1-1-0.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
 - SecHost.dll
 - API-MS-Win-Service-Core-Ansi-L1-1-1.dll
api_name:
 - GetServiceDisplayName
 - GetServiceDisplayNameA
 - GetServiceDisplayNameW
---

# GetServiceDisplayNameW function


## -description

Retrieves the display name of the specified service.

## -parameters

### -param hSCManager [in]

A handle to the service control manager database, as returned by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a> function.

### -param lpServiceName [in]

The service name. This name is the same as the service's registry key name. It is best to choose a name that is less than 256 characters.

### -param lpDisplayName [out, optional]

A pointer to a buffer that receives the service's display name. If the function fails, this buffer will contain an empty string.

The maximum size of this array is 4K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>lpcchBuffer</i> parameter. The function will fail and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return <b>ERROR_INSUFFICIENT_BUFFER</b>. The <i>lpcchBuffer</i> parameter will receive the required size.

This parameter can specify a localized string using the following format:

@[<i>path</i>\]<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. For more information, see <a href="/windows/desktop/api/winreg/nf-winreg-regloadmuistringa">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.

### -param lpcchBuffer [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by <i>lpDisplayName</i>, in <b>TCHARs</b>. 


On output, this variable receives the size of the service's display name, in characters, excluding the null-terminating character.

If the buffer pointed to by <i>lpDisplayName</i> is too small to contain the display name, the function does not store it. When the function returns, <i>lpcchBuffer</i> contains the size of the service's display name, excluding the null-terminating character.

## -returns

If the functions succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

There are two names for a service: the service name and the display name. The service name is the name of the service's key in the registry. The display name is a user-friendly name that appears in the Services control panel application, and is used with the <b>NET START</b> command. To map the service name to the display name, use the 
<b>GetServiceDisplayName</b> function. To map the display name to the service name, use the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-getservicekeynamea">GetServiceKeyName</a> function.





> [!NOTE]
> The winsvc.h header defines GetServiceDisplayName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-getservicekeynamea">GetServiceKeyName</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-openscmanagera">OpenSCManager</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>
