---
UID: NF:winsock.WSAStartup
title: WSAStartup function
author: windows-sdk-content
description: Initiates use of the Winsock DLL by a process.
old-location: winsock\wsastartup_2.htm
old-project: winsock
ms.assetid: 08299592-867c-491d-9769-d16602133659
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WSAStartup, WSAStartup function [Winsock], _win32_wsastartup_2, winsock.wsastartup_2, winsock/WSAStartup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: smiVENDORINFO, *smiLPVENDORINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
 - bcrypt.dll
 - wsock32.dll
api_name:
 - WSAStartup
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAStartup function


## -description


The 
<b>WSAStartup</b> function initiates use of the Winsock DLL by a process.


## -parameters




### -param wVersionRequired

TBD


### -param lpWSAData [out]

A pointer to the 
<a href="https://msdn.microsoft.com/c3c4c0d6-c8b3-4991-bedb-f45816cc8160">WSADATA</a> data structure that is to receive details of the Windows Sockets implementation.


#### - wVersionRequested [in]

The highest version of Windows Sockets specification that the caller can use. The high-order byte specifies the minor version number; the low-order byte specifies the major version number.


## -returns



If successful, the 
<b>WSAStartup</b> function returns zero. Otherwise, it returns one of the error codes listed below. 

The <b>WSAStartup</b> function directly returns the extended error code in the return value for this function. A call to the <a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function is not needed and should  not be used.
					

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSASYSNOTREADY</a></b></dt>
</dl>
</td>
<td width="60%">
The underlying network subsystem is not ready for network communication.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAVERNOTSUPPORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The version of Windows Sockets support requested is not provided by this particular Windows Sockets implementation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 operation is in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEPROCLIM</a></b></dt>
</dl>
</td>
<td width="60%">
A limit on the number of tasks supported by the Windows Sockets implementation has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpWSAData</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAStartup</b> function must be the first Windows Sockets function called by an application or DLL. It allows an application or DLL to specify the version of Windows Sockets required and retrieve details of the specific Windows Sockets implementation. The application or DLL can only issue further Windows Sockets functions after successfully calling 
<b>WSAStartup</b>.

In order to support various Windows Sockets implementations and applications that can have functional differences from the latest version of Windows Sockets specification, a negotiation takes place in 
<b>WSAStartup</b>. The caller of 
<b>WSAStartup</b> passes in the <i>wVersionRequested</i> parameter the highest version of the Windows Sockets specification that the application supports. The Winsock DLL indicates the highest version of the Windows Sockets specification that it can support in its response. The Winsock DLL also replies with version of the Windows Sockets specification that it expects the caller to use.

When an application or DLL calls the 
<b>WSAStartup</b> function, the Winsock DLL examines the version of the Windows Sockets specification requested by the application passed in the  <i>wVersionRequested</i> parameter. If the version requested by the application is equal to or higher than the lowest version supported by the Winsock DLL, the call succeeds and the Winsock DLL returns detailed information in the <a href="https://msdn.microsoft.com/c3c4c0d6-c8b3-4991-bedb-f45816cc8160">WSADATA</a> structure pointed to by the <i>lpWSAData</i> parameter. The <b>wHighVersion</b> member of the <b>WSADATA</b> structure indicates the highest version of the Windows Sockets specification that the Winsock DLL supports.  The <b>wVersion</b> member of the <b>WSADATA</b> structure indicates the version of the Windows Sockets specification that the Winsock DLL expects the caller to use.

If the <b>wVersion</b> member of the 
<a href="https://msdn.microsoft.com/c3c4c0d6-c8b3-4991-bedb-f45816cc8160">WSADATA</a> structure is unacceptable to the caller, the application or DLL should call 
<a href="https://msdn.microsoft.com/72b7cc3e-be34-41e7-acbf-61742149ec8b">WSACleanup</a> to release the Winsock DLL  resources and fail to initialize the Winsock application. In order to support this application or DLL,  it will be necessary to search for an updated version of the Winsock DLL to install on the platform. 

The current version of the Windows Sockets specification is version 2.2. The current Winsock DLL, <i>Ws2_32.dll</i>, supports applications that request  any of the following  versions of Windows Sockets specification: <ul>
<li>1.0</li>
<li>1.1</li>
<li>2.0</li>
<li>2.1</li>
<li>2.2</li>
</ul>


To get full access to the new syntax of a higher version of the Windows Sockets specification, the application must negotiate for this higher version. In this case, the <i>wVersionRequested</i> parameter should be set to request version 2.2.  The application must also fully conform to that higher version of the Windows Socket specification, such as compiling against the appropriate header file, linking with a new library, or other special cases. The <i>Winsock2.h header</i> file for Winsock 2 support is included with the Microsoft Windows Software Development Kit (SDK).

Windows Sockets version 2.2 is supported on Windows Server 2008, 
  Windows Vista, Windows Server 2003,
  Windows XP,
  Windows 2000, Windows NT 4.0 with Service Pack 4 (SP4) and later,
  Windows Me,
  Windows 98, and Windows 95 OSR2. 
  Windows Sockets version 2.2 is also supported on   
  Windows 95 with the Windows Socket 2 Update. Applications on these platforms should normally request Winsock 2.2 by setting the <i>wVersionRequested</i> parameter accordingly.

On Windows 95 and versions of Windows NT 3.51 and earlier, Windows Sockets version 1.1 is the highest version of the Windows Sockets specification supported. 

It is legal and possible for an application or DLL written to use a lower version of the Windows Sockets specification that is supported by the Winsock DLL to successfully negotiate this lower version using the  <b>WSAStartup</b> function. For example, an application can request version 1.1 in the <i>wVersionRequested</i> parameter passed to the <b>WSAStartup</b> function on a platform with the Winsock 2.2 DLL. In this case, the application should only rely on features that fit within the version requested. New Ioctl codes, new behavior of existing functions, and new functions should not be used. The version negotiation provided by the <b>WSAStartup</b> was primarily used to allow older Winsock 1.1 applications developed for Windows 95 and   Windows NT 3.51 and earlier to run with the same behavior on later versions of Windows. The <i>Winsock.h header</i> file for Winsock 1.1 support is included with the Windows SDK.

This negotiation in the <b>WSAStartup</b> function allows both the application or DLL that uses Windows Sockets  and the Winsock DLL to support a range of Windows Sockets versions. An application or DLL can use the Winsock DLL if there is any overlap in the version ranges. Detailed information on the Windows Sockets implementation is provided in the 
<a href="https://msdn.microsoft.com/c3c4c0d6-c8b3-4991-bedb-f45816cc8160">WSADATA</a> structure returned by the <b>WSAStartup</b> function.

The following table shows how 
<b>WSAStartup</b> works with different applications and Winsock DLL versions.<table>
<tr>
<th>Caller version support</th>
<th>Winsock DLL version support</th>
<th><b>wVersion </b> requested</th>
<th><b>wVersion </b> returned</th>
<th><b>wHighVersion </b>  returned</th>
<th>End result</th>
</tr>
<tr>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>1.0 1.1</td>
<td>1.0</td>
<td>1.1</td>
<td>1.0</td>
<td>1.0</td>
<td>use 1.0</td>
</tr>
<tr>
<td>1.0</td>
<td>1.0 1.1</td>
<td>1.0</td>
<td>1.0</td>
<td>1.1</td>
<td>use 1.0</td>
</tr>
<tr>
<td>1.1</td>
<td>1.0 1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>1.1</td>
<td>1.0</td>
<td>1.1</td>
<td>1.0</td>
<td>1.0</td>
<td>Application fails</td>
</tr>
<tr>
<td>1.0</td>
<td>1.1</td>
<td>1.0</td>
<td>—</td>
<td>—</td>
<td><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAVERNOTSUPPORTED</a></td>
</tr>
<tr>
<td>1.0 1.1</td>
<td>1.0 1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>1.1 2.0</td>
<td>1.0 1.1</td>
<td>2.0</td>
<td>1.1</td>
<td>1.1</td>
<td>use 1.1</td>
</tr>
<tr>
<td>2.0</td>
<td>1.0 1.1 2.0</td>
<td>2.0</td>
<td>2.0</td>
<td>2.0</td>
<td>use 2.0</td>
</tr>
<tr>
<td>2.0 2.2</td>
<td>1.0 1.1 2.0</td>
<td>2.2</td>
<td>2.0</td>
<td>2.0</td>
<td>use 2.0</td>
</tr>
<tr>
<td>2.2</td>
<td>1.0 1.1 2.0 2.1 2.2</td>
<td>2.2</td>
<td>2.2</td>
<td>2.2</td>
<td>use 2.2</td>
</tr>
</table>
 



Once an application or DLL has made a successful 
<b>WSAStartup</b> call, it can proceed to make other Windows Sockets calls as needed. When it has finished using the services of the Winsock DLL, the application must call 
<a href="https://msdn.microsoft.com/72b7cc3e-be34-41e7-acbf-61742149ec8b">WSACleanup</a> to allow the Winsock DLL to free internal Winsock resources used by the application.


An application can call 
<b>WSAStartup</b> more than once if it needs to obtain the 
<a href="https://msdn.microsoft.com/c3c4c0d6-c8b3-4991-bedb-f45816cc8160">WSADATA</a> structure information more than once. On each such call, the application can specify any version number supported by the Winsock DLL.

The 
<b>WSAStartup</b> function typically leads to protocol-specific helper DLLs being loaded. As a result, the 
<b>WSAStartup</b> function should not be called from the DllMain function in a application DLL. This can potentially cause deadlocks. For more information, please see the <a href="http://go.microsoft.com/fwlink/p/?linkid=109533">DLL Main Function</a>.

An application must call the <a href="https://msdn.microsoft.com/72b7cc3e-be34-41e7-acbf-61742149ec8b">WSACleanup</a> function for every successful 
time the <b>WSAStartup</b> function is called.  This means, for example, that if an application calls 
<b>WSAStartup</b> three times, it must call 
<b>WSACleanup</b> three times. The first two calls to 
<b>WSACleanup</b> do nothing except decrement an internal counter; the final 
<b>WSACleanup</b> call for the task does all necessary resource deallocation for the task.


<div class="alert"><b>Note</b>  An application can call the <a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function to determine the extended error code for other Windows sockets functions as is normally done in Windows Sockets even if 
the <b>WSAStartup</b> function fails or the <b>WSAStartup</b> function was not called to properly initialize Windows Sockets before calling a Windows Sockets function. The <b>WSAGetLastError</b> function is one of the only functions in the Winsock 2.2 DLL that can be called in the case of a <b>WSAStartup</b> failure. </div>
<div> </div>


<b>Windows Phone 8:</b> This  function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

The following code fragment demonstrates how an application that supports only version 2.2 of Windows Sockets makes a 
<b>WSAStartup</b> call:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define WIN32_LEAN_AND_MEAN

#include &lt;windows.h&gt;
#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;stdio.h&gt;

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")


int __cdecl main()
{

    WORD wVersionRequested;
    WSADATA wsaData;
    int err;

/* Use the MAKEWORD(lowbyte, highbyte) macro declared in Windef.h */
    wVersionRequested = MAKEWORD(2, 2);

    err = WSAStartup(wVersionRequested, &amp;wsaData);
    if (err != 0) {
        /* Tell the user that we could not find a usable */
        /* Winsock DLL.                                  */
        printf("WSAStartup failed with error: %d\n", err);
        return 1;
    }

/* Confirm that the WinSock DLL supports 2.2.*/
/* Note that if the DLL supports versions greater    */
/* than 2.2 in addition to 2.2, it will still return */
/* 2.2 in wVersion since that is the version we      */
/* requested.                                        */

    if (LOBYTE(wsaData.wVersion) != 2 || HIBYTE(wsaData.wVersion) != 2) {
        /* Tell the user that we could not find a usable */
        /* WinSock DLL.                                  */
        printf("Could not find a usable version of Winsock.dll\n");
        WSACleanup();
        return 1;
    }
    else
        printf("The Winsock 2.2 dll was found okay\n");
        

/* The Winsock DLL is acceptable. Proceed to use it. */

/* Add network programming using Winsock here */

/* then call WSACleanup when done using the Winsock dll */
    
    WSACleanup();

}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/ms632663(v=VS.85).aspx">MAKEWORD</a>



<a href="https://msdn.microsoft.com/72b7cc3e-be34-41e7-acbf-61742149ec8b">WSACleanup</a>



<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>



<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>
 

 

