---
UID: NF:winsvc.GetServiceDisplayNameW
title: GetServiceDisplayNameW function
author: windows-sdk-content
description: Retrieves the display name of the specified service.
old-location: base\getservicedisplayname.htm
tech.root: services
ms.assetid: 704812f3-134c-4161-b3b4-a955d87ff563
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetServiceDisplayName, GetServiceDisplayName function, GetServiceDisplayNameA, GetServiceDisplayNameW, _win32_getservicedisplayname, base.getservicedisplayname, winsvc/GetServiceDisplayName, winsvc/GetServiceDisplayNameA, winsvc/GetServiceDisplayNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetServiceDisplayNameW function


## -description


Retrieves the display name of the specified service.


## -parameters




### -param hSCManager [in]

A handle to the service control manager database, as returned by the 
<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a> function.


### -param lpServiceName [in]

The service name. This name is the same as the service's registry key name. It is best to choose a name that is less than 256 characters.


### -param lpDisplayName [out, optional]

A pointer to a buffer that receives the service's display name. If the function fails, this buffer will contain an empty string.

The maximum size of this array is 4K bytes. To determine the required size, specify NULL for this parameter and 0 for the <i>lpcchBuffer</i> parameter. The function will fail and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return <b>ERROR_INSUFFICIENT_BUFFER</b>. The <i>lpcchBuffer</i> parameter will receive the required size.

This parameter can specify a localized string using the following format:

@[<i>path</i>\]<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. For more information, see <a href="https://msdn.microsoft.com/76ffc77f-a1bc-4e01-858f-4a76563a2bbc">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.


### -param lpcchBuffer [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by <i>lpDisplayName</i>, in <b>TCHARs</b>. 


On output, this variable receives the size of the service's display name, in characters, excluding the null-terminating character.

If the buffer pointed to by <i>lpDisplayName</i> is too small to contain the display name, the function does not store it. When the function returns, <i>lpcchBuffer</i> contains the size of the service's display name, excluding the null-terminating character.


## -returns



If the functions succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



There are two names for a service: the service name and the display name. The service name is the name of the service's key in the registry. The display name is a user-friendly name that appears in the Services control panel application, and is used with the <b>NET START</b> command. To map the service name to the display name, use the 
<b>GetServiceDisplayName</b> function. To map the display name to the service name, use the 
<a href="https://msdn.microsoft.com/d2421566-de4a-49e5-bb41-ea98c6f6d19d">GetServiceKeyName</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d2421566-de4a-49e5-bb41-ea98c6f6d19d">GetServiceKeyName</a>



<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

