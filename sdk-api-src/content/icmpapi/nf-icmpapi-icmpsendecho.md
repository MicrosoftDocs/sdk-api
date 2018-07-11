---
UID: NF:icmpapi.IcmpSendEcho
title: IcmpSendEcho function
author: windows-sdk-content
description: The IcmpSendEcho function sends an IPv4 ICMP echo request and returns any echo response replies. The call returns when the time-out has expired or the reply buffer is filled.
old-location: iphlp\icmpsendecho.htm
old-project: iphlp
ms.assetid: c3cdc535-2c13-48c6-9ab1-88cc5e5119b5
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IcmpSendEcho, IcmpSendEcho function [IP Helper], _iphlp_icmpsendecho, icmpapi/IcmpSendEcho, iphlp.icmpsendecho
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: icmpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
 - Icmp.dll
api_name:
 - IcmpSendEcho
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP; Icmp.dll on Windows 2000 Server and Windows 2000 Professional
req.irql: 
req.product: GDI+ 1.1
---

# IcmpSendEcho function


## -description


The 
<b>IcmpSendEcho</b> function sends an IPv4 ICMP echo request and returns any echo response replies. The call returns when the time-out has expired or the reply buffer is filled.


## -parameters




### -param IcmpHandle [in]

The open handle returned by the <a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a> function.


### -param DestinationAddress [in]

The IPv4 destination address of the echo request, in the form of an <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a> structure.


### -param RequestData [in]

A pointer to a buffer that contains data to send in the request.


### -param RequestSize [in]

The size, in bytes, of the request data buffer pointed to by the <i>RequestData</i> parameter.


### -param RequestOptions [in, optional]

A pointer to the IP header options for the request, in the form of an <a href="https://msdn.microsoft.com/4341d0a4-65d8-4677-b208-2cde5ff36f14">IP_OPTION_INFORMATION</a> structure. On a 64-bit platform, this parameter is in the form for an <a href="https://msdn.microsoft.com/3924230d-ff10-43ac-981c-81273bce6896">IP_OPTION_INFORMATION32</a> structure.

This parameter may be <b>NULL</b> if no IP header options need to be specified.




### -param ReplyBuffer [out]

A buffer to hold any replies to the echo request. Upon return, the buffer contains an array of 
<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a> structures followed by the options and data for the replies. The buffer should be large enough to hold at least one 
<b>ICMP_ECHO_REPLY</b> structure plus <i>RequestSize</i> bytes of data.

On a 64-bit platform, upon return the buffer contains an array of <a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a> structures followed by the options and data for the replies.


### -param ReplySize [in]

The allocated size, in bytes,  of the reply buffer. The buffer should be large enough to hold at least one 
<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a> structure plus <i>RequestSize</i> bytes of data. On a 64-bit platform, The buffer should be large enough to hold at least one 
<a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a> structure plus <i>RequestSize</i> bytes of data.

This buffer should also be large enough to also hold 8 more bytes of data (the size of an ICMP error message).



### -param Timeout [in]

The time, in milliseconds, to wait for replies.


## -returns



The 
						<b>IcmpSendEcho</b> function returns the number of 
<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a> or <a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a> structures stored in the <i>ReplyBuffer</i>. The status of each reply is contained in the structure. If the return value is zero, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for additional error information.

If the function fails, the extended error code returned by <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The data area passed to a system call is too small. This error is returned if the <i>ReplySize</i> parameter indicates that the buffer pointed to by the <i>ReplyBuffer</i> parameter is too small. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>IcmpHandle</i> parameter contains an invalid handle. This error can also be returned if the <i>ReplySize</i> parameter specifies a value less than the size of an <a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a> or <a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IP_BUF_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>ReplyBuffer</i> specified in the <i>ReplySize</i> parameter was too small.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>IcmpSendEcho</b> function send an ICMP echo request to the specified address and returns the number of replies received and stored in <i>ReplyBuffer</i>.  The <b>IcmpSendEcho</b> function is a synchronous function and returns after waiting for the time specified in the <i>Timeout</i> parameter for a response. If the return value is zero, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for extended error information.

The <a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a> and <a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a> functions are enhanced version of <b>IcmpSendEcho</b> that support asynchronous operation. The <b>IcmpSendEcho2Ex</b> function also allows the source IP address to be specified. This feature is useful on computers with multiple network interfaces.

For IPv6, use the <a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>, <a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>, and <a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a> functions.

The <b>IcmpSendEcho</b> function is exported from the <i>Icmp.dll</i> on Windows 2000. The <b>IcmpSendEcho</b> function is exported from the <i>Iphlpapi.dll</i> on Windows XP and later. Windows version checking is not recommended to use this function. Applications requiring portability  with this function across Windows 2000, Windows XP, Windows Server 2003 and later Windows versions should not statically link to either the <i>Icmp.lib</i> or the <i>Iphlpapi.lib</i> file. Instead, the application should check for the presence of <b>IcmpSendEcho</b> in the <i>Iphlpapi.dll</i> with calls to <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.  Failing that, the application should check for the presence of <b>IcmpSendEcho</b> in the <i>Icmp.dll</i> with  calls to <b>LoadLibrary</b> and <b>GetProcAddress</b>. 

Note that the include directive for <i>Iphlpapi.h</i> header file must be placed before the <i>Icmpapi.h</i> header file.


#### Examples

The following example sends an ICMP echo request to the IP address specified on the command line and prints the information received from the first response.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;winsock2.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;icmpapi.h&gt;
#include &lt;stdio.h&gt;

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

int __cdecl main(int argc, char **argv)  {

    // Declare and initialize variables
    
    HANDLE hIcmpFile;
    unsigned long ipaddr = INADDR_NONE;
    DWORD dwRetVal = 0;
    char SendData[32] = "Data Buffer";
    LPVOID ReplyBuffer = NULL;
    DWORD ReplySize = 0;
    
    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s IP address\n", argv[0]);
        return 1;
    }

    ipaddr = inet_addr(argv[1]);
    if (ipaddr == INADDR_NONE) {
        printf("usage: %s IP address\n", argv[0]);
        return 1;
    }
    
    hIcmpFile = IcmpCreateFile();
    if (hIcmpFile == INVALID_HANDLE_VALUE) {
        printf("\tUnable to open handle.\n");
        printf("IcmpCreatefile returned error: %ld\n", GetLastError() );
        return 1;
    }    

    ReplySize = sizeof(ICMP_ECHO_REPLY) + sizeof(SendData);
    ReplyBuffer = (VOID*) malloc(ReplySize);
    if (ReplyBuffer == NULL) {
        printf("\tUnable to allocate memory\n");
        return 1;
    }    
    
    
    dwRetVal = IcmpSendEcho(hIcmpFile, ipaddr, SendData, sizeof(SendData), 
        NULL, ReplyBuffer, ReplySize, 1000);
    if (dwRetVal != 0) {
        PICMP_ECHO_REPLY pEchoReply = (PICMP_ECHO_REPLY)ReplyBuffer;
        struct in_addr ReplyAddr;
        ReplyAddr.S_un.S_addr = pEchoReply-&gt;Address;
        printf("\tSent icmp message to %s\n", argv[1]);
        if (dwRetVal &gt; 1) {
            printf("\tReceived %ld icmp message responses\n", dwRetVal);
            printf("\tInformation from the first response:\n"); 
        }    
        else {    
            printf("\tReceived %ld icmp message response\n", dwRetVal);
            printf("\tInformation from this response:\n"); 
        }    
        printf("\t  Received from %s\n", inet_ntoa( ReplyAddr ) );
        printf("\t  Status = %ld\n", 
            pEchoReply-&gt;Status);
        printf("\t  Roundtrip time = %ld milliseconds\n", 
            pEchoReply-&gt;RoundTripTime);
    }
    else {
        printf("\tCall to IcmpSendEcho failed.\n");
        printf("\tIcmpSendEcho returned error: %ld\n", GetLastError() );
        return 1;
    }
    return 0;
}    
    
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a>



<a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>



<a href="https://msdn.microsoft.com/4341d0a4-65d8-4677-b208-2cde5ff36f14">IP_OPTION_INFORMATION</a>



<a href="https://msdn.microsoft.com/3924230d-ff10-43ac-981c-81273bce6896">IP_OPTION_INFORMATION32</a>



<a href="https://msdn.microsoft.com/2ddb23d8-a4e6-47c4-a552-2815ccaf055f">Icmp6CreateFile</a>



<a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a>



<a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>



<a href="https://msdn.microsoft.com/ce8f11bb-1e33-41bd-adb9-c18efadd4d0b">IcmpCloseHandle</a>



<a href="https://msdn.microsoft.com/b435b38b-df86-4991-9772-c712c9ea606f">IcmpCreateFile</a>



<a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a>



<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>



<a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>
 

 

