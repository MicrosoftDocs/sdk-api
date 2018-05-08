---
UID: NF:winsock.WSAGetLastError
title: WSAGetLastError function
author: windows-driver-content
description: Returns the error status for the last Windows Sockets operation that failed.
old-location: winsock\wsagetlasterror_2.htm
old-project: WinSock
ms.assetid: 39e41b66-44ed-46dc-bfc2-65228b669992
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: WSAGetLastError, WSAGetLastError function [Winsock], _win32_wsagetlasterror_2, winsock.wsagetlasterror_2, winsock/WSAGetLastError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsock.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: smiVENDORINFO, *smiLPVENDORINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ws2_32.dll
api_name:
-	WSAGetLastError
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAGetLastError function


## -description


The 
<b>WSAGetLastError</b> function returns the error status for the last Windows Sockets operation that failed.


## -parameters






## -returns




						The return value indicates the error code for this thread's last Windows Sockets operation that failed.




## -remarks



The 
<b>WSAGetLastError</b> function returns the last error that occurred for the calling thread. When a particular Windows Sockets function indicates an error has occurred, this function should be called immediately to retrieve the extended error code for the failing function call. This extended error code can be different from the error code obtained from 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> when called with an <i>optname</i> parameter of <b>SO_ERROR</b>, which is socket-specific since 
<b>WSAGetLastError</b> is for all thread-specific sockets.

If a function call's return value indicates that error or other relevant data was returned in the error code, <b>WSAGetLastError</b> should be called immediately. This is necessary because some functions may  reset the last extended error code to 0 if they succeed, overwriting the extended error code returned by a previously failed function. To specifically reset the extended error code, use the 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a> function call with the <i>iError</i> parameter set to zero. A 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> function when called with an <i>optname</i> parameter of <b>SO_ERROR</b> also resets the extended error code to zero.

The 
<b>WSAGetLastError</b> function should not be used to check for an extended error value on receipt of an asynchronous message. In this case, the extended error value is passed in the <i>lParam</i> parameter of the message, and this can differ from the value returned by 
<b>WSAGetLastError</b>.


<div class="alert"><b>Note</b>  An application can call the <b>WSAGetLastError</b> function to determine the extended error code for other Windows sockets functions as is normally done in Windows Sockets even if 
the <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> function fails or the <b>WSAStartup</b> function was not called to properly initialize Windows Sockets before calling a Windows Sockets function. The <b>WSAGetLastError</b> function is one of the only functions in the Winsock 2.2 DLL that can be called in the case of a <b>WSAStartup</b> failure. </div>
<div> </div>


The Windows Sockets extended error codes returned by this function and the text description of the error are listed under <a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">Windows Sockets Error Codes</a>. These error codes and a short text description associated with an error code are defined in the <i>Winerror.h</i> header file. The <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function can be used to obtain the message string for the returned error.

For information on how to handle error codes when porting socket applications to Winsock, see <a href="https://msdn.microsoft.com/cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1">Error Codes - errno, h_errno and WSAGetLastError</a>. 
		

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1">Error Codes - errno, h_errno and WSAGetLastError</a>



<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">Windows Sockets Error Codes</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>
 

 

